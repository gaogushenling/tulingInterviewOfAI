# 依赖注入

<font style="color:rgb(0, 0, 0);">依赖注入（Dependency Injection, DI）是软件开发中的一种设计模式，它可以使代码更加松耦合、便于测试和维护。在Java开发中，尤其是在Spring框架中，依赖注入扮演着非常重要的角色。</font>

# <font style="color:rgb(0, 0, 0);">1. 什么是依赖注入</font>
<font style="color:rgb(0, 0, 0);">依赖注入是一种设计模式，其核心思想是</font>**<font style="color:rgb(0, 0, 0);">将对象的创建和对其依赖的管理交给外部容器</font>**<font style="color:rgb(0, 0, 0);">，而不是在内部进行管理。这促进了松耦合，使得代码更易于测试和维护。</font>

# <font style="color:rgb(0, 0, 0);">2. 依赖注入的三种方式</font>
+ **<font style="color:rgb(0, 0, 0);">构造器注入</font>**<font style="color:rgb(0, 0, 0);">: 通过构造函数提供依赖对象。</font>
+ **<font style="color:rgb(0, 0, 0);">Setter方法注入</font>**<font style="color:rgb(0, 0, 0);">: 通过Setter方法提供依赖对象。</font>
+ **<font style="color:rgb(0, 0, 0);">字段注入</font>**<font style="color:rgb(0, 0, 0);">: 通过属性字段提供依赖对象。</font>

# <font style="color:rgb(0, 0, 0);">3. Spring中的依赖注入</font>
<font style="color:rgb(0, 0, 0);">Spring框架是Java领域最著名的依赖注入框架。它通过配置文件或注解配置来管理对象的生命周期和依赖关系。</font>

## <font style="color:rgb(0, 0, 0);">3.1 Spring中的构造器注入</font>
### <font style="color:rgb(0, 0, 0);">示例代码</font>
```java
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.context.annotation.ComponentScan;
import org.springframework.context.annotation.Configuration;
import org.springframework.stereotype.Component;

@Component
class ServiceA {
    // Service implementation
}
@Component
class ServiceB {
    private  ServiceA serviceA;
    @Autowired
    public ServiceB(ServiceA serviceA) {
        this.serviceA = serviceA;
    }
    public void performTask() {
        // Use serviceA to perform some task
        System.out.println(this.serviceA);
    }
}
```

## <font style="color:rgb(0, 0, 0);">3.2 Spring中的Setter方法注入</font>
### <font style="color:rgb(0, 0, 0);">示例代码</font>
```java
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.context.annotation.ComponentScan;
import org.springframework.context.annotation.Configuration;
import org.springframework.stereotype.Component;
@Component
class ServiceA {
    // Service implementation
}
@Component
class ServiceB {
    private ServiceA serviceA;
    @Autowired
    public void setServiceA(ServiceA serviceA) {
        this.serviceA = serviceA;
    }
    public void performTask() {
        // Use serviceA to perform some task
        System.out.println(this.serviceA);
    }
}
```

## <font style="color:rgb(0, 0, 0);">3.3 Spring中的字段注入</font>
### <font style="color:rgb(0, 0, 0);">示例代码</font>
```java
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.context.annotation.ComponentScan;
import org.springframework.context.annotation.Configuration;
import org.springframework.stereotype.Component;
@Component
class ServiceA {
    // Service implementation
}
@Component
class ServiceB {
    @Autowired
    private ServiceA serviceA;
    public void performTask() {
        // Use serviceA to perform some task
        System.out.println(this.serviceA);
    }
}
```

### 




> 更新: 2025-04-20 22:39:00  
> 原文: <https://www.yuque.com/aaron-wecc3/dhluml/peazspypgpmg2beh>