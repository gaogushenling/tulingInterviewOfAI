# 某读书会Redis 大Key引发的线上事故分析总结

# 背景

某读书会运营一个在线阅读平台，用户可以创建自己的读书记录并分享书评。为了提高性能，系统使用Redis作为存储层，存储热门用户的读书记录数据。然而，运营期间，系统在某天晚上突然出现严重的延迟和关闭超时，直接影响了用户体验。

***

# 一、事故分析

## 1. 事故现象

* 平台API响应时间从正常的50ms激增至5s。
* 数据库负载异常增加，读写次数激增。
* Redis 的`INFO`输出显示内存使用率异常高，且响应时间大大延长。

## 2. 根本原因

经检查，问题源于某个Redis服务器键（大key）。该键存储了一个用户的所有读书排记录，采用`hash`类型，记录了数万条数据，大小超过**100 MB**。由于以下原因，大键导致了性能问题：

* **获取大Key**：读取整个哈希类型数据导致阻塞。
* **中间逐出问题**：大Key被Redis淘汰时，导致主线程阻塞，其他请求被延迟。
* **网络延迟**：关键数据量过大，传输时间过长。
* **重建存储**：每次重新计算大Key，数据库查询压力激增。

***

# 二、解决方案

## 1.核心思路

* **定位大键**：快速找到导致问题的大key。
* **拆分优化**：将大Key操作拆分为多个小Key，减少每次的体积。
* **实时监控**：构建Redis大关键监控机制，预防类似问题。

***

## 2.实现步骤

### （1）定位大键 可以通过以下Lua脚本快速扫描Redis并定位大键：

```lua
-- scan_big_key.lua
local cursor = "0"
local big_keys = {}
repeat
    local result = redis.call("SCAN", cursor, "COUNT", 100)
    cursor = result[1]
    local keys = result[2]
    for _, key in ipairs(keys) do
        local key_type = redis.call("TYPE", key).ok
        local key_size = 0
        if key_type == "string" then
            key_size = redis.call("STRLEN", key)
        elseif key_type == "hash" then
            key_size = redis.call("HLEN", key)
        elseif key_type == "list" then
            key_size = redis.call("LLEN", key)
        elseif key_type == "set" then
            key_size = redis.call("SCARD", key)
        elseif key_type == "zset" then
            key_size = redis.call("ZCARD", key)
        end
        if key_size > 10000 then -- 自定义大Key阈值
            table.insert(big_keys, {key, key_type, key_size})
        end
    end
until cursor == "0"
return big_keys

```

运行结果可快速定位占用内存大的键。

***

### （2）优化大关键 发现问题后，可以采用以下方式拆分：

1. **按用户分片**：大键中的`hash`按用户ID分片，例如`user:read_logs:1000`。
2. **分页存储**：限制每个关键存储的边界数，例如`user:read_logs:1000:page1`。

以下是示例代码：

```java
import redis.clients.jedis.Jedis;

import java.util.List;

public class RedisKeyOptimizer {
    public static void main(String[] args) {
        try (Jedis jedis = new Jedis("localhost", 6379)) {
            String largeHashKey = "user:profile:1002";
            int pageSize = 1000; // 每页存储 1000 条记录

            // 拆分大Key
            List<String> fields = jedis.hkeys(largeHashKey).stream().toList();
            for (int i = 0; i < fields.size(); i += pageSize) {
                int end = Math.min(i + pageSize, fields.size());
                List<String> subFields = fields.subList(i, end);
                String newKey = largeHashKey + ":page" + (i / pageSize);
                subFields.forEach(field -> {
                    String value = jedis.hget(largeHashKey, field);
                    jedis.hset(newKey, field, value);
                });
                jedis.expire(newKey, 3600); // 设置过期时间为1小时
            }

            // 删除原始大Key
            jedis.del(largeHashKey);

            System.out.println("Large key optimized successfully.");
        }
    }
}

```

### （3）值班与警卫

* 使用Redis的`INFO keyspace`命令监控按键数量和内存占用。
* 定期运行Lua脚本扫描大键，并设置报警。

***

# 三、优化后的结果

## 性能提升：

```
- API响应恢复至50ms左右。
- 数据库压力急剧下降，QPS恢复正常。
```

## 可维护性增强：

```
- 大关键问题被拆分后，运维更加轻松。
- 实现了Redis按键大小的实时监控。
```

# 四、案例总结

## 经验教训

1. **合理设计缓存结构**：避免单个大关键，提前规划分片策略。
2. **限制键大小**：设置明确的大键警戒线，提前排查问题。
3. **构建监控机制**：线上系统必须具备实时预警和自愈能力。

## 技术要点

1. 使用Redis的Lua脚本快速定位问题。
2. 结合Java分片存储技术分割大关键。
3. 定期对Redis做健康检查，避免潜在的风险。

## 总结语

Redis 是高性能存储的利器，但使用不当会引发灾难性后果。通过合理的设计、及时的监控和科学的运维，能够最大化 Redis 的性能，为业务保驾护航。

:::info

:::

测试数据创建

通过Java代码创建Redis数据：

```java
import redis.clients.jedis.Jedis;

public class RedisTestDataGenerator {
    public static void main(String[] args) {
        try (Jedis jedis = new Jedis("localhost", 6379)) {
            jedis.flushDB(); // 清空数据库，确保干净的环境

            // 1. 创建一个大 Hash Key
            String largeHashKey = "user:profile:1002";
            for (int i = 0; i < 15000; i++) {
                jedis.hset(largeHashKey, "field" + i, "value" + i);
            }

            // 2. 创建一个超大的 List Key
            String largeListKey = "logs:events";
            for (int i = 0; i < 500000; i++) {
                jedis.rpush(largeListKey, "log_event_" + i);
            }

            // 3. 创建几个小 Key
            jedis.set("session:data", "short_string_data");
            jedis.hset("user:profile:1001", "field1", "value1");
            jedis.hset("user:profile:1001", "field2", "value2");
            jedis.rpush("user:activity", "login");
            jedis.rpush("user:activity", "logout");

            System.out.println("Test data successfully created in Redis.");
        }
    }
}
```

MySQL 测试数据

```plsql
CREATE TABLE user_read_logs (
    id INT AUTO_INCREMENT PRIMARY KEY,
    user_id VARCHAR(255) NOT NULL,
    book_title VARCHAR(255) NOT NULL,
    read_time TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

以下 SQL 脚本会为用户 1002 插入 15,000 条读书记录：

```plsql
INSERT INTO user_read_logs (user_id, book_title)
SELECT '1002', CONCAT('Book Title ', seq)
FROM (SELECT @row := @row + 1 AS seq FROM (SELECT 1 UNION ALL SELECT 2 UNION ALL SELECT 3 UNION ALL SELECT 4) t1,
      (SELECT 1 UNION ALL SELECT 2 UNION ALL SELECT 3 UNION ALL SELECT 4) t2,
      (SELECT 1 UNION ALL SELECT 2 UNION ALL SELECT 3 UNION ALL SELECT 4) t3,
      (SELECT 1 UNION ALL SELECT 2 UNION ALL SELECT 3 UNION ALL SELECT 4) t4,
      (SELECT @row := 0) t0 LIMIT 15000) seq_table;
```


> 更新: 2025-04-20 22:38:59  
> 原文: <https://www.yuque.com/aaron-wecc3/dhluml/ma6mg2fo6p5omeig>