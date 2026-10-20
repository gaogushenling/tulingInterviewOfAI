# Java实现多线程的方式，手写

1. <font style="color:rgb(0, 0, 0);">继承Thread类</font>
2. <font style="color:rgb(0, 0, 0);">实现Runnable接口</font>
3. <font style="color:rgb(0, 0, 0);">实现Callable接口并配合Future与ExecutorService使用</font>

<font style="color:rgb(0, 0, 0);">下面我将详细介绍每种方式，并提供相应的示例代码。</font>

### <font style="color:rgb(0, 0, 0);">1. 继承Thread类</font>
<font style="color:rgb(0, 0, 0);">继承</font>Thread<font style="color:rgb(0, 0, 0);">类并重写</font>run()<font style="color:rgb(0, 0, 0);">方法是实现多线程的最简单方式之一。</font>

```java
class MyThread extends Thread {

    @Override

    public void run() {

        for (int i = 0; i < 5; i++) {

            System.out.println(Thread.currentThread().getName() + " is running: " + i);

        }

    }

    public static void main(String[] args) {

        MyThread t1 = new MyThread();

        MyThread t2 = new MyThread();

        t1.start();

        t2.start();

    }

}
```

### <font style="color:rgb(0, 0, 0);">2. 实现Runnable接口</font>
<font style="color:rgb(0, 0, 0);">实现</font>Runnable<font style="color:rgb(0, 0, 0);">接口并将其实例传递给</font>Thread<font style="color:rgb(0, 0, 0);">对象。</font>

```java
class MyRunnable implements Runnable {

    @Override

    public void run() {

        for (int i = 0; i < 5; i++) {

            System.out.println(Thread.currentThread().getName() + " is running: " + i);

        }

    }

    public static void main(String[] args) {

        Thread t1 = new Thread(new MyRunnable());

        Thread t2 = new Thread(new MyRunnable());

        t1.start();

        t2.start();

    }

}
```

### <font style="color:rgb(0, 0, 0);">3. 实现Callable接口并配合Future与ExecutorService使用</font>
Callable<font style="color:rgb(0, 0, 0);">接口与</font>Runnable<font style="color:rgb(0, 0, 0);">接口的不同在于，</font>Callable<font style="color:rgb(0, 0, 0);">可以返回执行结果，并且可以抛出异常。通常与</font>Future<font style="color:rgb(0, 0, 0);">和</font>ExecutorService<font style="color:rgb(0, 0, 0);">一同使用</font>

```java
import java.util.concurrent.Callable;

import java.util.concurrent.ExecutionException;

import java.util.concurrent.ExecutorService;

import java.util.concurrent.Executors;

import java.util.concurrent.Future;

class MyCallable implements Callable<Integer> {

    @Override

    public Integer call() throws Exception {

        int sum = 0;

        for (int i = 0; i < 5; i++) {

            sum += i;

            System.out.println(Thread.currentThread().getName() + " is running: " + i);

        }

        return sum;

    }

    public static void main(String[] args) {

        ExecutorService executor = Executors.newFixedThreadPool(2);

        Future<Integer> future1 = executor.submit(new MyCallable());

        Future<Integer> future2 = executor.submit(new MyCallable());

        try {

            System.out.println("Result of future1: " + future1.get());

            System.out.println("Result of future2: " + future2.get());

        } catch (InterruptedException | ExecutionException e) {

            e.printStackTrace();

        }

        executor.shutdown();

    }

}
```

### <font style="color:rgb(0, 0, 0);">小结</font>
<font style="color:rgb(0, 0, 0);">上述三种方式各有优缺点：</font>

1. **<font style="color:rgb(0, 0, 0);">继承Thread类</font>**<font style="color:rgb(0, 0, 0);">:</font>
    - <font style="color:rgb(0, 0, 0);">优点: 简单，直接继承</font>Thread<font style="color:rgb(0, 0, 0);">类即可。</font>
    - <font style="color:rgb(0, 0, 0);">缺点: Java只允许单继承，如果已经继承了其他类就无法再继承</font>Thread<font style="color:rgb(0, 0, 0);">。</font>
2. **<font style="color:rgb(0, 0, 0);">实现Runnable接口</font>**<font style="color:rgb(0, 0, 0);">:</font>
    - <font style="color:rgb(0, 0, 0);">优点: 可以避免单继承的局限性。</font>
    - <font style="color:rgb(0, 0, 0);">缺点: 无法直接获得执行结果。</font>
3. **<font style="color:rgb(0, 0, 0);">实现Callable接口</font>**<font style="color:rgb(0, 0, 0);">:</font>
    - <font style="color:rgb(0, 0, 0);">优点: 可以返回结果或抛出异常。</font>
    - <font style="color:rgb(0, 0, 0);">缺点: 需要配合</font>Future<font style="color:rgb(0, 0, 0);">和</font>ExecutorService<font style="color:rgb(0, 0, 0);">，相对复杂一些。</font>

<font style="color:rgb(0, 0, 0);">选择哪种方式取决于具体需求，如果需要返回结果或处理异常推荐使用</font>Callable<font style="color:rgb(0, 0, 0);">接口，如果只是简单的多线程操作</font>Runnable<font style="color:rgb(0, 0, 0);">接口足够。</font>



> 更新: 2025-04-20 22:39:02  
> 原文: <https://www.yuque.com/aaron-wecc3/dhluml/os9hfimg96fmp93z>