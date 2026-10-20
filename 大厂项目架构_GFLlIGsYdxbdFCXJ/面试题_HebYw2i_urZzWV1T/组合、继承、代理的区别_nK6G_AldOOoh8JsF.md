# 组合、继承、代理的区别

<font style="color:rgb(0, 0, 0);">在Java编程中，组合（Composition）、继承（Inheritance）和代理（Delegation）是实现代码复用和对象关系的重要方式。它们各有特点和适用场景，以下是它们的区别和使用方式：</font>

### <font style="color:rgb(0, 0, 0);">1. 组合（Composition）</font>
<font style="color:rgb(0, 0, 0);">组合是指一个类包含另一个类的实例作为其成员变量，从而通过这个成员变量来实现功能。换句话说，组合是一种“has-a”（有一个）关系。</font>

**<font style="color:rgb(0, 0, 0);">优点：</font>**

+ <font style="color:rgb(0, 0, 0);">组合提供了更灵活的设计，因为可以在运行时决定对象的组合。</font>
+ <font style="color:rgb(0, 0, 0);">它允许类之间的耦合度较低，因为类之间没有强制的继承关系，只是基于接口或实现类进行协作。</font>

**<font style="color:rgb(0, 0, 0);">示例代码：</font>**

```java
public class Composition {
    public static void main(String[] args) {
        Car car = new Car();
        car.startCar();
    }
}

class Engine {
    void start() {
        System.out.println("Engine start");
    }
}
class Car {
    private Engine engine = new Engine();
    void startCar() {
        engine.start();
        System.out.println("Car started");
    }
}

```

### <font style="color:rgb(0, 0, 0);">2. 继承（Inheritance）</font>
<font style="color:rgb(0, 0, 0);">继承是面向对象编程中的一种机制，一个类可以继承另一个类的属性和方法，从而实现代码复用和扩展。继承是一种“is-a”（是一种）关系。</font>

**<font style="color:rgb(0, 0, 0);">优点：</font>**

+ <font style="color:rgb(0, 0, 0);">让子类复用父类的代码，提高代码的复用性。</font>
+ <font style="color:rgb(0, 0, 0);">子类可以通过继承父类来扩展和扩充功能。</font>

**<font style="color:rgb(0, 0, 0);">缺点：</font>**

+ <font style="color:rgb(0, 0, 0);">继承使得子类和父类之间耦合度较高，当父类发生变化时，子类可能也需要相应地改变。</font>
+ <font style="color:rgb(0, 0, 0);">Java 不支持多重继承。</font>

**<font style="color:rgb(0, 0, 0);">示例代码：</font>**

```java
public class Inheritance {
    public static void main(String[] args) {
        Dog dog = new Dog();
        dog.makeSound(); // Outputs "Woof"
    }
}

class Animal {
    void makeSound() {
        System.out.println("Animal sound");
    }
}
class Dog extends Animal {
    @Override
    void makeSound() {
        System.out.println("Woof");
    }
}
```

### <font style="color:rgb(0, 0, 0);">3. 代理（Delegation）</font>
<font style="color:rgb(0, 0, 0);">代理模式是一种设计模式，它允许一个对象为另外一个对象提供代理访问。代理通常用来控制对对象的访问，可以用于延迟初始化、访问控制等场景。代理是一种“delegate-to”（委派到）关系。</font>

**<font style="color:rgb(0, 0, 0);">优点：</font>**

+ <font style="color:rgb(0, 0, 0);">通过代理可以在不改变原有类的情况下扩展功能。</font>
+ <font style="color:rgb(0, 0, 0);">可以对对象的访问进行控制，如添加日志、权限控制等。</font>

<font style="color:rgb(0, 0, 0);">我们可以通过代理模式实现对某个对象的</font>**<font style="color:rgb(0, 0, 0);">访问控制</font>**<font style="color:rgb(0, 0, 0);">，例如验证权限。</font>

**<font style="color:rgb(0, 0, 0);">示例代码：</font>**

```java
// Subject接口
public interface Subject {
    void request();
}
// RealSubject类
public class RealSubject implements Subject {
    public void request() {
        System.out.println("RealSubject: Handling request.");
    }
}
// Proxy类
public class Proxy implements Subject {
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
            System.out.println("Proxy: Access denied. Only Admin can access.");
        }
    }
}
// 客户端代码
public class Client {
    public static void main(String[] args) {
        Proxy proxy = new Proxy("User");
        proxy.request();  // 输出：Proxy: Access denied. Only Admin can access.
        Proxy adminProxy = new Proxy("Admin");
        adminProxy.request();  // 输出：RealSubject: Handling request.
    }
}
```

### <font style="color:rgb(0, 0, 0);">总结</font>
+ **<font style="color:rgb(0, 0, 0);">组合</font>**<font style="color:rgb(0, 0, 0);">强调的是“has-a”(有一个)关系，使用成员变量来表示两个类之间的关系。</font>
+ **<font style="color:rgb(0, 0, 0);">继承</font>**<font style="color:rgb(0, 0, 0);">强调的是“is-a”(是一种)关系，使用继承来实现代码复用和多态性。</font>
+ **<font style="color:rgb(0, 0, 0);">代理</font>**<font style="color:rgb(0, 0, 0);">则是通过一个代理对象来间接访问真正的目标对象，常用于控制访问、延迟初始化等场景。</font>

<font style="color:rgb(0, 0, 0);">根据具体情况选择合适的方式，可以提高代码的可维护性和复用性。</font>



> 更新: 2025-04-20 22:39:01  
> 原文: <https://www.yuque.com/aaron-wecc3/dhluml/hq6kieui6q96dpdh>