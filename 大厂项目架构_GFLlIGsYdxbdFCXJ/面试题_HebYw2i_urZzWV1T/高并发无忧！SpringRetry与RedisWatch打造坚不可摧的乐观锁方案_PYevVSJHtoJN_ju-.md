# 高并发无忧！Spring Retry 与 Redis Watch 打造坚不可摧的乐观锁方案

# 背景及业务场景描述

在电商抢购或秒杀活动中，当大量用户同时请求抢购相同商品时，通常会面临以下挑战：

1. **瞬时**请求量极大。
2. **数据一致性**：库存数量必须准确扣减，不能超卖。
3. **性能要求高**：需要减少数据库的访问和锁竞争。

传统方案可能会使用数据库的行级锁或全局锁机制，但对性能要求高的场景可能会遇到瓶颈。Redis作为内存存储，在高并发场景中可以起到流量削峰快速及访问的作用。而Redis提供的`WATCH`命令可以用于实现乐观锁定，实现实际库存扣减时的并发安全。

# 技术选择及方法

* **Redis**：作为库存统计的存储介质。
* **WATCH + MULTI/EXEC**：通过在扣减库存时对Redis的键进行监控（WATCH），如果在执行事务（MULTI/EXEC）期间该键被其他客户端修改了  ，则事务修改执行失败，客户端可选择重试。
* **Spring Retry**：在出现执行失败时，自动触发重试，重试次数及指定事务策略，保证在高并发机制冲突下仍有较好的成功率。
* **Spring Boot + Spring Data Redis**：简化Redis的操作，使用`StringRedisTemplate`redis键值来操作。

# 代码结构与依赖Maven依赖（示例）

```java
<dependencies>
    <!-- Spring Boot Starter Web -->
    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-web</artifactId>
    </dependency>
    <!-- Spring Data Redis -->
    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-data-redis</artifactId>
    </dependency>
    <!-- Spring Retry -->
    <dependency>
        <groupId>org.springframework.retry</groupId>
        <artifactId>spring-retry</artifactId>
    </dependency>
    <!-- Lombok(可选) -->
    <dependency>
        <groupId>org.projectlombok</groupId>
        <artifactId>lombok</artifactId>
        <optional>true</optional>
    </dependency>
</dependencies>
```

# 配置文件（application.yml）

```java
spring:
  redis:
    host: localhost
    port: 6379
  # 示例：根据业务需要配置连接池，超时等

# 开启spring retry全局支持
spring:
  main:
    allow-bean-definition-overriding: true
```

# 启用Spring Retry注意事项

## 在应用主类或配置类中启用`@EnableRetry`

```java
import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;
import org.springframework.retry.annotation.EnableRetry;

@SpringBootApplication
@EnableRetry
public class SeckillApplication {
    public static void main(String[] args) {
        SpringApplication.run(SeckillApplication.class, args);
    }
}
```

# 业务实现细节

## 服务逻辑描述

设想一个商品ID为`product:1001`，对应的库存键为`stock:product:1001`在Redis中维护。

初始值（活动开始前在Redis中设置）

```java
SET stock:product:1001 10  # 设置初始库存10
```

在用户下单时，需要执行以下步骤：

1. 从Redis中读取当前库存值，如果库存值> 0，则有资格尝试减减。
2. 使用`WATCH`命令控制`stock:product:1001`键。
3. 开启Redis事务（`MULTI`），尝试`DECR`操作执行将库存减少1。
4. 执行`EXEC`提交事务，如果`EXEC`在前面该键携带其他人修改，`EXEC`返回成功，否则返回null或失败，说明有并发冲突。
5. 对并发冲突进行重试（Spring Retry）。在短时间内（如毫秒级）自动多次重试可以最大程度提高成功率。
6. 成功扣减后返回下单成功信息，若库存为0则提示库存不足。

## 代码示例

### 服务层示例（库存扣减逻辑）

```java
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.data.redis.connection.RedisStringCommands;
import org.springframework.data.redis.core.StringRedisTemplate;
import org.springframework.data.redis.core.SessionCallback;
import org.springframework.retry.annotation.Backoff;
import org.springframework.retry.annotation.Retryable;
import org.springframework.stereotype.Service;

@Service
public class SeckillService {

    @Autowired
    private StringRedisTemplate redisTemplate;
    
    private static final String STOCK_KEY_PREFIX = "stock:product:";

    /**
     * 尝试扣减库存
     * @param productId 产品ID
     * @return true表示扣减成功，false表示库存不足或扣减失败
     */
    @Retryable(
        value = {IllegalStateException.class}, // 当执行事务失败（返回null）时会抛出自定义异常
        maxAttempts = 5, // 最大重试5次
        backoff = @Backoff(delay = 10) // 重试间隔10毫秒，可根据情况调整
    )
    public boolean tryDecreaseStock(String productId) {
        String stockKey = STOCK_KEY_PREFIX + productId;

        // 1. 读取库存
        String currentStockStr = redisTemplate.opsForValue().get(stockKey);
        if (currentStockStr == null) {
            throw new IllegalStateException("库存键不存在");
        }
        
        int currentStock = Integer.parseInt(currentStockStr);
        if (currentStock <= 0) {
            // 库存不足
            return false;
        }

        // 2. 开始watch
        return redisTemplate.execute(new SessionCallback<Boolean>() {
            @Override
            public Boolean execute(org.springframework.data.redis.core.RedisOperations operations) {
                operations.watch(stockKey);
                // 再次检查库存(这里可以省略，因为上面已经获取了currentStock，但watch后取值更保险)
                String val = (String) operations.opsForValue().get(stockKey);
                int stock = Integer.parseInt(val);
                if (stock <= 0) {
                    operations.unwatch(); // 没有必要继续事务
                    return false;
                }

                // 3. 开启事务
                operations.multi();
                operations.opsForValue().increment(stockKey, -1);
                // 4. 提交事务
                Object execResult = operations.exec();
                
                if (execResult == null) {
                    // 表示watch的key在exec前已被修改，乐观锁冲突，抛出异常触发retry
                    throw new IllegalStateException("事务执行失败，触发重试");
                }

                // execResult 是一个List，包含执行MULTI/EXEC中的操作结果
                // 正常情况下只有一个decrement操作
                // 返回的第一个结果需要判断是否成功
                return true;
            }
        });
    }
}
```

在上述代码中，有几个重点：

* 使用`@Retryable`注解，当`IllegalStateException`发送时间会自动重试。
* 在执行事务时，如果`exec()`返回`null`，说明乐观锁冲突。我们通过发送`IllegalStateException`来让Spring Retry进行重试。
* 重试次数和延迟可以根据实际场景进行调整。

### Controller 层示例

```java
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.web.bind.annotation.*;

@RestController
@RequestMapping("/seckill")
public class SeckillController {

    @Autowired
    private SeckillService seckillService;

    @GetMapping("/buy")
    public String buy(@RequestParam String productId) {
        boolean result = seckillService.tryDecreaseStock(productId);
        if (result) {
            return "恭喜，下单成功！";
        } else {
            return "很抱歉，库存不足或下单失败。";
        }
    }
}
```

# 总结

本案例通过Spring Retry与Redis Watch乐观锁的组合实现了高并发场景下的可靠库存扣减。具体内容如下：

* **Redis修改的WATCH**保证在二进制相同键时，只能有一个事务提交成功，其他线程回滚失败。
* **Spring Retry**自动处理失败的重试逻辑，从而在高并发场景下消耗手动处理业务回滚后再次尝试的复杂逻辑。
* **性能与一致性的平衡**：使用内存级的Redis操作和乐观锁使得在高并发下仍然能够保持较高的性能和更好的数据一致性。


> 更新: 2025-04-20 22:38:57  
> 原文: <https://www.yuque.com/aaron-wecc3/dhluml/ckaoglm1410ru8z3>