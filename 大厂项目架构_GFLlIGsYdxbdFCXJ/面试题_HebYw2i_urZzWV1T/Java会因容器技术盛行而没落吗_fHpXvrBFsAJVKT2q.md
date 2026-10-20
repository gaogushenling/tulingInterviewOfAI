# Java会因容器技术盛行而没落吗

## 背景：
<font style="color:rgb(77, 77, 77);">近年来以容器为核心的云原生技术，让服务端部署的伸缩性、可协作性，得到巨大的提升。使得原本开发语言本身选取的重要性，有一定程度的减弱。但不妨碍Java语言本身继续保持活力。</font>

容器的出现，改变了代码的运行模式，促进了[云原生](https://www.zhihu.com/search?q=%E4%BA%91%E5%8E%9F%E7%94%9F&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A2738569054%7D)的发展。与语言无关。容器具有以下优势。

+ 降低开销  
容器采用一个应用一个进程的模式在操作系统上运行。容器采用的LXC实现隔离。cgroups实现资源分配，底层本质上还是有同一套操作系统。与传统或硬件虚拟机环境相比，容器所需的系统资源更少，因为它们不包含操作系统映像。
+ 标准化，可移植  
只要符合开放容器标准（OCI）的应用就可以通过容器运行。
+ 便捷的环境管理  
容器提供了一系列的API操作，可以对容器的资源分配，部署运行等进行管理。



诚然容器的出现，通过制定一套标准的方式来实现了跨平台,且不少大厂也有项目go取代java。但Java还有其他不可忽视的优势。跨平台只是Java语言里面应用并不广泛的特性，所以不会因为容器技术盛行而没落。



## 跨平台
实际上，在后端并没有太多的应用场景需要 Java 跨平台，大多数的 Java 后端服务都运行在 x64 Linux 环境上。真正需要关注跨平台的是客户端编程，但这个领域中 Java 的份额相对较小，而且也不会经常用到 Docker。



Docker 和 Kubernetes（k8s）的兴起实际上更多是为了方便管理和部署，Docker 只是在 Linux 核心之上添加了一层薄薄的映射，它主要省去的是配置环境的时间，而不是减少代码在运行时跨平台的问题。Docker 并不是专门用来处理跨平台问题的工具，它更多是用来解决环境依赖的问题。



而 Kubernetes 则更侧重于集群资源管理，这对于所有支持微服务的语言都是有益的，当然也包括 Java。

## <font style="color:rgb(25, 27, 31);">性能方面</font>
+ <font style="color:rgb(25, 27, 31);">运行性能</font>

<font style="color:rgb(25, 27, 31);">The Benchmarks Game选择了目前热门的25种语言做了</font>[<font style="color:rgb(25, 27, 31);">性能测试</font>](https://link.zhihu.com/?target=https%3A//goodmanwen.github.io/Programming-Language-Benchmarks-Visualization)<font style="color:rgb(25, 27, 31);">。</font>

![1723034951407-f21698ec-8daf-4db4-92a1-8b71e67125ee.png](./img/fHpXvrBFsAJVKT2q/1723034951407-f21698ec-8daf-4db4-92a1-8b71e67125ee-120235.png)

<font style="color:rgb(25, 27, 31);">可见，Java的运行性能并不差，并且性能也并不是语言流行的重要标准（Python虽然性能垫底，但由于其简单性，还是世界上使用最广泛的语言）。</font>



+ 启动性能

Java由于在启动时，需要加载.class文件，并通过JIT编译成机器码，导致其启动性能差。针对这一点，JVM通过提前编译来进行了优化。特别是GraalVM的Native Image，还做了最新的即时优化，导致启动速度大幅度提升。GraalVM针对云原生的特性，尽可能的缩小了必要的jvm体积。

Java不会随着容器的兴起而没落，相反，容器的兴起也许会给Java带来新的可能性。

  
 

## 生态体系
庞大而完整的生态系统  
Java作为一门开源的老牌语言，拥有众多开发人员。积累了丰富的资源，拥有庞大的第三方类库Maven的[Central Repository](https://link.zhihu.com/?target=https%3A//mvnrepository.com/repos/central)上已经有近千万的packages。拥有庞大的生态系统和社区支持，这为Java开发者提供了丰富的库、框架和工具。Java无论是Spring、Hibernate等主流框架，还是Maven、Gradle等构建工具，都为Java开发者提供了高效、便捷的开发体验。此外，Java社区还积极推动开源文化和知识共享，为Java的未来发展提供了强大的动力。Java也应用于各个领域，包含桌面应用（AWT，Swing，JavaFX等），服务端应用，Web应用（Servlet，JSP），云应用，移动应用（Android）等等。

在高并发或大数据吞吐量的情况下，各种后端语言，包括 C/C++，都会遇到各种问题。但在大多数后端应用场景下，Java 是最成熟的解决方案，同时也遇到的问题（包括性能问题）相对较少。这可以很容易理解，经过长时间的实践，一条被走得多的路往往更平坦。虽然也有人会提到 C/C++，但在相同复杂度的逻辑下，C/C++ 编程对程序员的负担更重，就像攀登珠峰的道路，再多的人也难以将其变得平坦。

## 与时俱进
         JDK保持着每半年发布一次新版本。面向对象编程，自动垃圾回收，提前编译，[函数式编程](https://www.zhihu.com/search?q=%E5%87%BD%E6%95%B0%E5%BC%8F%E7%BC%96%E7%A8%8B&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A2738569054%7D)，协程。等等  
Java衍生出众多优秀框架。比如spring，springboot，hadoop等等。

Java 的成功也得益于高质量的 JVM 和 Java 程序员对常用框架和库的持续优化。Java 的内存模型和运行效率实际上是很高的。只是有一些“爱用”某些框架的 Java 程序员可能会遇到低效的情况，或者有些框架被滥用。另外，有时候问题并不在语言本身，而是在所处理的问题规模上，比如一个运行了几天的 Hadoop 作业，用 C++ 重写可能会引入更多问题并且运行更慢。此时，更应该考虑的是调整算法，而不是仅仅改变编程语言。因此，关于性能问题，实际上并不存在“锅”，即使存在也不能完全归咎于 Java。











> 更新: 2024-08-07 21:06:00  
> 原文: <https://www.yuque.com/aaron-wecc3/dhluml/aa8qkxggxocw50x8>