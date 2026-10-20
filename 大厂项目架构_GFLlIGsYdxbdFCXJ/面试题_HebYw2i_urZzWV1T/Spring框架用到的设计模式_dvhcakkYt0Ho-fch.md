# Spring框架用到的设计模式

<font style="color:rgb(0, 0, 0);">Spring框架作为一个广泛使用的Java企业应用开发框架，使用了许多设计模式来实现其灵活性和扩展性。以下是一些在Spring中常见的设计模式：</font>

1. **<font style="color:rgb(0, 0, 0);">单例模式（Singleton Pattern）</font>**<font style="color:rgb(0, 0, 0);">： Spring默认情况下，Bean是单例的。也就是说，Spring容器会确保每个Bean只有一个实例，该实例在整个应用中会被共享使用。</font>

```java
package com.tuling.interview.Spring框架用到的设计模式.单例模式;

public class Singleton {

    private volatile static   Singleton singleton  = null;

    //私有构造
    private Singleton(){

    }
    
    public static Singleton getSingleton(){
        if(singleton == null){
            synchronized (Singleton.class){
               if(singleton == null){
                   singleton = new Singleton();
               }
            }
        }
        return singleton;
    }


}
```

**<font style="color:rgb(0, 0, 0);">2.工厂模式（Factory Pattern）</font>**<font style="color:rgb(0, 0, 0);">： Spring中的</font>BeanFactory<font style="color:rgb(0, 0, 0);">和</font>ApplicationContext<font style="color:rgb(0, 0, 0);">是工厂模式的典型例子，它们用于创建和管理Bean的实例。</font>

```java
package com.tuling.interview.Spring框架用到的设计模式.工厂模式;

public class Factory {


    public static void main(String[] args) {

        ProductFactory productFactory = new ProductFactory();

        // 创建 ProductA 对象

        Product productA = productFactory.createProduct("A");

        productA.create();

        // 创建 ProductB 对象

        Product productB = productFactory.createProduct("B");

        productB.create();

    }


}



// 定义产品接口
interface Product {

    void create();

}

// 实现类 ProductA
class ProductA implements Product {

    @Override

    public void create() {

        System.out.println("ProductA is created.");

    }

}

// 实现类 ProductB
class ProductB implements Product {

    @Override

    public void create() {

        System.out.println("ProductB is created.");

    }
}


class ProductFactory {

    // 工厂方法，根据参数类型创建具体的产品对象

    public Product createProduct(String type) {

        if (type.equalsIgnoreCase("A")) {

            return new ProductA();

        } else if (type.equalsIgnoreCase("B")) {

            return new ProductB();

        }

        // 可以返回 null 或者抛出异常

        return null;

    }

}
```

**<font style="color:rgb(0, 0, 0);">3.代理模式（Proxy Pattern）</font>**<font style="color:rgb(0, 0, 0);">： Spring AOP（面向切面编程）大量使用了代理模式。当你配置一个切面（Aspect）时，Spring会创建目标对象的代理来拦截方法调用，并在方法执行前后插入额外的行为。</font>

```java
/**
 * 上面的代码展示了如何通过代理模式实现对对象的访问控制（权限验证）
 */
public class Client {

    public static void main(String[] args) {
        Proxy proxy = new Proxy("User");
        proxy.request();  // 输出：抱歉，你没有权限！
        Proxy adminProxy = new Proxy("Admin");
        adminProxy.request();  // 输出：得到请求的权限！
    }
}

// Subject接口
interface Subject {
    void request();
}

// RealSubject类
 class RealSubject implements Subject {
    public void request() {
        System.out.println("得到请求的权限！");
    }
}

// Proxy类
class Proxy implements Subject {
    private RealSubject realSubject;
    private String userRole;
    public Proxy(String userRole) {
        this.userRole = userRole;
    }
    public void request() {
        // 进行权限检查
        if (this.userRole.equals("Admin")) {
            if (realSubject == null) {
                realSubject = new RealSubject();
            }
            realSubject.request();
        } else {
            System.out.println("抱歉，你没有权限！");
        }
    }
}
```

**<font style="color:rgb(0, 0, 0);"> 4.模板模式（Template Pattern）</font>**<font style="color:rgb(0, 0, 0);">： Spring提供许多模板类（如</font>JdbcTemplate<font style="color:rgb(0, 0, 0);">、</font>RestTemplate<font style="color:rgb(0, 0, 0);">、</font>JpaTemplate<font style="color:rgb(0, 0, 0);">等）来减少与特定技术（如JDBC、REST、JPA等）交互的样板代码。</font>

```java
package com.tuling.interview.Spring框架用到的设计模式.模板模式;

public class Template {


    public static void main(String[] args) {

        Game game = new Cricket();

        game.play();  // 使用模板方法来调用算法骨架

        System.out.println("=======");

        game = new Football();

        game.play();  // 使用模板方法来调用算法骨架

    }
}


// 抽象类定义模板方法和抽象步骤

abstract class Game {

    // 模板方法，不可改变的算法骨架

    public final void play() {

        initialize();

        startPlay();

        endPlay();

    }

    // 抽象步骤方法

    abstract void initialize();

    abstract void startPlay();

    abstract void endPlay();

}

// 具体子类实现抽象步骤方法

class Cricket extends Game {

    @Override

    void initialize() {

        System.out.println("Cricket Game initialize.");

    }

    @Override

    void startPlay() {

        System.out.println("Cricket Game startPlay.");

    }
    @Override

    void endPlay() {

        System.out.println("Cricket Game endPlay.");

    }

}

class Football extends Game {

    @Override

    void initialize() {

        System.out.println("Football Game initialize.");

    }

    @Override

    void startPlay() {

        System.out.println("Football Game startPlay.");

    }
    @Override

    void endPlay() {

        System.out.println("Football Game endPlay.");

    }

}
```

**<font style="color:rgb(0, 0, 0);">5.装饰者模式（Decorator Pattern）</font>**<font style="color:rgb(0, 0, 0);">： Spring的</font>BeanPostProcessor<font style="color:rgb(0, 0, 0);">允许在Bean初始化之前和之后对Bean进行处理或修改，这类似于装饰者模式。</font>

```java
public class CustomBeanPostProcessor implements BeanPostProcessor {

    @Override

    public Object postProcessBeforeInitialization(Object bean, String beanName) throws BeansException {

        // 在Bean初始化之前的处理

        return bean;

    }

    @Override

    public Object postProcessAfterInitialization(Object bean, String beanName) throws BeansException {

        // 在Bean初始化之后的处理

        return bean;

    }

}
```

**<font style="color:rgb(0, 0, 0);">6.观察者模式（Observer Pattern）</font>**<font style="color:rgb(0, 0, 0);">： Spring的事件机制（如</font>ApplicationEvent<font style="color:rgb(0, 0, 0);">和</font>ApplicationListener<font style="color:rgb(0, 0, 0);">）就是观察者模式的实现。事件发布者（Subject）会通知所有注册的监听器（Observer），使它们能够对事件进行响应。</font>

```java
/**
 * 定义事件: 首先你需要定义一个事件类，继承ApplicationEvent：
 */
public class CustomEvent extends ApplicationEvent {

    private String message;
    public CustomEvent(Object source,String message) {
        super(source);
        this.message =message;
    }


    public String getMessage(){
        return message;
    }
}


/**
 * 发布事件: 最后，使用ApplicationEventPublisher来发布事件。可以在任何Spring管理的Bean中注入ApplicationEventPublisher，然后调用publishEvent方法发布事件。
 */
@Component
public class CustomEventPublisher {

    @Autowired
    private ApplicationEventPublisher applicationEventPublisher;

    public void publishEvent(final String message) {


        CustomEvent customEvent = new CustomEvent(this, message);

        applicationEventPublisher.publishEvent(customEvent);

    }
}



/**
 * 定义监听器: 接下来，定义一个监听器类，实现ApplicationListener接口，并重写onApplicationEvent方法。
 */
@Component
public class CustomEventListener  implements ApplicationListener<CustomEvent> {
    @Override
    public void onApplicationEvent(CustomEvent event) {
        System.out.println("Received custom event - " + event.getMessage());
    }
}
```

**<font style="color:rgb(0, 0, 0);">7.依赖注入模式（Dependency Injection Pattern）</font>**<font style="color:rgb(0, 0, 0);">： 这是Spring框架的核心设计模式之一，通过构造函数注入、Setter方法注入或接口注入的方式，Spring实现了松耦合设计。</font>

**<font style="color:rgb(0, 0, 0);">8.适配器模式（Adapter Pattern）</font>**<font style="color:rgb(0, 0, 0);">： Spring通过</font>HandlerAdapter<font style="color:rgb(0, 0, 0);">将不同类型的处理器统一适配到</font>DispatcherServlet<font style="color:rgb(0, 0, 0);">，从而实现请求的处理。</font>

**<font style="color:rgb(0, 0, 0);">9.策略模式（Strategy Pattern）</font>**<font style="color:rgb(0, 0, 0);">： Spring内部使用了策略模式来实现不同的策略行为，例如Spring的事务管理使用不同的事务策略来处理事务边界。</font>

**<font style="color:rgb(0, 0, 0);">10.组合模式（Composite Pattern）</font>**<font style="color:rgb(0, 0, 0);">： Spring中使用组合模式来组合多个</font>BeanPostProcessor<font style="color:rgb(0, 0, 0);">或多个Advice（在AOP中）来实现复杂的功能。</font>

<font style="color:rgb(0, 0, 0);">这些设计模式一起工作，帮助Spring提供一个强大且灵活的开发平台，使得开发者能够构建易于维护、扩展和测试的企业级应用程序。</font>



> 更新: 2025-04-20 22:39:01  
> 原文: <https://www.yuque.com/aaron-wecc3/dhluml/taq8dmn7nwo4agl9>