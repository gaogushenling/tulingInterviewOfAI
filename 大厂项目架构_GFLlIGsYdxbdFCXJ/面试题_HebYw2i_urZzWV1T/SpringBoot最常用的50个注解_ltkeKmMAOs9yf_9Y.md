# SpringBoot 最常用的50个注解

  
<font style="color:rgb(43, 43, 43);">SpringBoot提供了很多注解，可以快速构建应用程序。以下是SpringBoot最常用的50个注解：</font>  
**<font style="color:rgb(43, 43, 43);">1）@SpringBootApplication</font>**  
<font style="color:rgb(43, 43, 43);">作用：这是一个组合注解，包括了@Configuration、@EnableAutoConfiguration和@ComponentScan三个注解。用于标识SpringBoot应用程序的入口类。</font>  
●**<font style="color:rgb(53, 148, 247);">@Configuration</font>**<font style="color:rgb(43, 43, 43);">：指示这个类是一个配置类，它定义了一个或多个@Bean方法，用于创建和配置Spring应用程序上下文中的Bean。</font>  
●**<font style="color:rgb(53, 148, 247);">@EnableAutoConfiguration</font>**<font style="color:rgb(43, 43, 43);">：启用Spring Boot的自动配置机制，它会自动添加所需的依赖项和配置，以使应用程序能够运行。</font>  
●**<font style="color:rgb(53, 148, 247);">@ComponentScan</font>**<font style="color:rgb(43, 43, 43);">：指示Spring Boot扫描当前包及其子包中的所有@Component、@Service、@Repository和@Controller注解的类，并将它们注册为Spring Bean。</font>  
<font style="color:rgb(43, 43, 43);">@SpringBootApplication注解通常被用于Spring Boot应用程序的入口类上，用于启动Spring Boot应用程序。它可以简化Spring应用程序的配置和启动过程。</font>  
<font style="color:rgb(43, 43, 43);">用例：</font>  
**<font style="color:rgb(43, 43, 43);">2）@RestController</font>**  
<font style="color:rgb(43, 43, 43);">作用：与@Controller类似，但是@RestController会自动将返回值转换为JSON格式。</font>  
<font style="color:rgb(43, 43, 43);">@RestController是Spring Framework 4.0版本引入的一个注解，它是@Controller和@ResponseBody的组合注解。它用于标注一个类，表示这个类是一个RESTful风格的控制器，可以处理HTTP请求并返回JSON/XML格式的响应。</font>  
<font style="color:rgb(43, 43, 43);">@RestController注解用于替代原来的@Controller注解，它默认情况下会将控制器方法的返回值转换为JSON格式，并以HTTP响应的方式返回给客户端。如果需要返回XML格式的响应，可以使用其他注解，如@Produces和@Consumes。</font>  
<font style="color:rgb(43, 43, 43);">用例：</font>  
**<font style="color:rgb(43, 43, 43);">3）@RequestMapping</font>**  
<font style="color:rgb(43, 43, 43);">作用：用于映射请求URL和处理方法。@RequestMapping是Spring MVC框架中的一个核心注解，它用于映射HTTP请求和控制器方法之间的关系。它可以用于类级别和方法级别，用于指定请求URL和HTTP方法（GET、POST、PUT、DELETE等）。</font>  
<font style="color:rgb(43, 43, 43);">用例：</font>  
**<font style="color:rgb(43, 43, 43);">4）@GetMapping</font>**  
<font style="color:rgb(43, 43, 43);">作用：用于映射HTTP GET请求。</font>  
<font style="color:rgb(43, 43, 43);">用例：</font>  
**<font style="color:rgb(43, 43, 43);">5）@PostMapping</font>**  
<font style="color:rgb(43, 43, 43);">作用：用于映射HTTP POST请求。</font>  
<font style="color:rgb(43, 43, 43);">用例：</font>  
**<font style="color:rgb(43, 43, 43);">6）@PutMapping</font>**  
<font style="color:rgb(43, 43, 43);">作用：用于映射HTTP PUT请求。</font>  
<font style="color:rgb(43, 43, 43);">用例：</font>  
**<font style="color:rgb(43, 43, 43);">7）@DeleteMapping</font>**  
<font style="color:rgb(43, 43, 43);">作用：用于映射HTTP DELETE请求。</font>  
<font style="color:rgb(43, 43, 43);">用例：</font>  
**<font style="color:rgb(43, 43, 43);">8）@RequestParam</font>**  
<font style="color:rgb(43, 43, 43);">作用：用于获取请求参数的值。</font>  
<font style="color:rgb(43, 43, 43);">用例：</font>  
**<font style="color:rgb(43, 43, 43);">9）@PathVariable</font>**  
<font style="color:rgb(43, 43, 43);">作用：用于获取URL中的参数值。@PathVariable是Spring MVC框架中的一个注解，用于将HTTP请求路径中的变量绑定到控制器方法的参数上。</font>  
<font style="color:rgb(43, 43, 43);">用例：</font>  
**<font style="color:rgb(43, 43, 43);">10）@RequestBody</font>**  
<font style="color:rgb(43, 43, 43);">作用：用于将HTTP请求的主体转换为方法的参数。@RequestBody是Spring MVC框架中的一个注解，用于将HTTP请求体中的数据绑定到控制器方法的参数上。</font>  
<font style="color:rgb(43, 43, 43);">用例：</font>  
**<font style="color:rgb(43, 43, 43);">11）@ResponseBody</font>**  
<font style="color:rgb(43, 43, 43);">作用：用于将方法的返回值转换为HTTP响应的主体。@ResponseBody是Spring MVC框架中的一个注解，用于将控制器方法的返回值转换为HTTP响应体中的数据。</font>  
<font style="color:rgb(43, 43, 43);">用例：</font>  
**<font style="color:rgb(43, 43, 43);">12）@Autowired</font>**  
<font style="color:rgb(43, 43, 43);">作用：用于自动装配Spring容器中的Bean。</font>  
<font style="color:rgb(43, 43, 43);">用例：</font>  
**<font style="color:rgb(43, 43, 43);">13）@Component</font>**  
<font style="color:rgb(43, 43, 43);">作用：用于标识一个类是Spring容器中的组件。@Component是Spring框架中的一个通用注解，用于标注一个类作为Spring Bean。</font>  
<font style="color:rgb(43, 43, 43);">用例：</font>  
**<font style="color:rgb(43, 43, 43);">14）@Service</font>**  
<font style="color:rgb(43, 43, 43);">作用：用于标识一个类是Spring容器中的服务组件。@Service是Spring框架中的一个注解，用于标注一个类作为服务类（Service）。</font>  
<font style="color:rgb(43, 43, 43);">用例：</font>  
**<font style="color:rgb(43, 43, 43);">15）@Repository</font>**  
<font style="color:rgb(43, 43, 43);">作用：用于标识一个类是Spring容器中的数据访问组件。@Repository是Spring框架中的一个注解，用于标注一个类作为数据访问对象（DAO）。</font>  
<font style="color:rgb(43, 43, 43);">用例：</font>  
**<font style="color:rgb(43, 43, 43);">16）@Configuration</font>**  
<font style="color:rgb(43, 43, 43);">作用：用于标识一个类是Spring的配置类。@Configuration是Spring框架中的一个注解，用于标注一个类作为配置类。</font>  
<font style="color:rgb(43, 43, 43);">用例：</font>  
**<font style="color:rgb(43, 43, 43);">17）@Value</font>**  
<font style="color:rgb(43, 43, 43);">作用：用于获取配置文件中的属性值。@Value是Spring框架中的一个注解，用于将配置文件中的属性值注入到Bean对象中。</font>  
<font style="color:rgb(43, 43, 43);">用例：</font>  
<font style="color:rgb(43, 43, 43);">这个类使用@Component注解标注，表示这个类是一个Spring Bean，可以被其他的Spring Bean自动装配。</font>  
<font style="color:rgb(43, 43, 43);">在属性级别上，@Value注解指定了需要注入的属性值，这个属性值可以通过${...}的方式引用配置文件中的属性值。</font>  
<font style="color:rgb(43, 43, 43);">在这个例子中，MyComponent类中的myProperty属性使用@Value注解指定了需要注入的属性值，Spring会自动将配置文件中名为my.property的属性值注入到这个属性中。</font>  
<font style="color:rgb(43, 43, 43);">@Value注解用于注入配置文件中的属性值，使得开发者可以方便地从配置文件中获取属性值，并将其注入到Bean对象中。同时，使用@Value注解还可以方便地处理不同环境下的配置文件，如开发环境和生产环境的配置文件。</font>  
<font style="color:rgb(43, 43, 43);">@Value注解是Spring框架中比较常用的注解之一，可以让开发者更加专注于业务逻辑的实现，而不必关心属性值的获取和注入细节。</font>  
**<font style="color:rgb(43, 43, 43);">18）@Bean</font>**  
<font style="color:rgb(43, 43, 43);">作用：用于将一个方法返回的对象注册到Spring容器中。@Bean是Spring框架中的一个注解，用于将一个方法返回的对象注册为一个Spring Bean。</font>  
<font style="color:rgb(43, 43, 43);">用例：</font>  
**<font style="color:rgb(43, 43, 43);">19）@Import</font>**  
<font style="color:rgb(43, 43, 43);">作用：用于导入其他配置类或Bean。</font>  
<font style="color:rgb(43, 43, 43);">用例：</font>  
**<font style="color:rgb(43, 43, 43);">20）@Conditional</font>**  
<font style="color:rgb(43, 43, 43);">作用：用于根据条件判断是否创建Bean或执行配置。</font>  
<font style="color:rgb(43, 43, 43);">用例：</font>  
**<font style="color:rgb(43, 43, 43);">21）@Profile</font>**  
<font style="color:rgb(43, 43, 43);">作用：用于指定配置的环境，如开发环境、测试环境或生产环境。</font>  
<font style="color:rgb(43, 43, 43);">用例：</font>  
**<font style="color:rgb(43, 43, 43);">22）@PropertySource</font>**  
<font style="color:rgb(43, 43, 43);">作用：用于指定配置文件的位置。@PropertySource是Spring框架中的一个注解，用于指定一组属性文件的位置，从而可以在Spring应用程序中使用这些属性。</font>  
<font style="color:rgb(43, 43, 43);">用例：</font>  
<font style="color:rgb(43, 43, 43);">这个类使用@Configuration注解标注，表示这个类是一个配置类，用于配置应用程序的Bean对象。</font>  
<font style="color:rgb(43, 43, 43);">在类级别上，使用@PropertySource注解可以指定一个属性文件的位置。在这个例子中，使用@PropertySource注解指定了一个名为application.properties的属性文件，它位于classpath下。</font>  
<font style="color:rgb(43, 43, 43);">在方法级别上，使用@Bean注解标注方法，表示这个方法返回一个Bean对象。在这个例子中，使用Environment对象从属性文件中读取属性值，并将这些属性值传递给UserService实例的构造方法。</font>  
<font style="color:rgb(43, 43, 43);">@PropertySource注解用于指定一组属性文件的位置，使得开发者可以在Spring应用程序中使用这些属性。同时，使用Environment对象可以方便地读取属性文件中的属性值，并将这些属性值传递给Bean对象的构造方法或属性。</font>  
<font style="color:rgb(43, 43, 43);">@PropertySource注解是Spring框架中比较常用的注解之一，可以让开发者更加灵活地管理和配置Spring Bean。</font>  
**<font style="color:rgb(43, 43, 43);">23）@Qualifier</font>**  
<font style="color:rgb(43, 43, 43);">作用：用于指定注入的Bean的名称。</font>  
<font style="color:rgb(43, 43, 43);">用例：</font>  
**<font style="color:rgb(43, 43, 43);">24）@ExceptionHandler</font>**  
<font style="color:rgb(43, 43, 43);">作用：用于处理异常。</font>  
<font style="color:rgb(43, 43, 43);">用例：</font>  
<font style="color:rgb(43, 43, 43);">这个类使用@ControllerAdvice注解标注，表示这个类是一个全局异常处理器。在方法级别上，使用@ExceptionHandler注解可以指定一个方法来处理控制器中抛出的异常。</font>  
<font style="color:rgb(43, 43, 43);">在这个例子中，使用@ExceptionHandler注解指定了一个名为handleException的方法，它处理所有类型的异常。当控制器中抛出异常时，会调用这个方法，并将异常对象作为参数传递给这个方法。</font>  
<font style="color:rgb(43, 43, 43);">在这个方法中，使用ModelAndView对象来封装错误信息，并将视图名称设置为error。最后，返回这个ModelAndView对象，将错误信息显示到用户界面上。</font>  
<font style="color:rgb(43, 43, 43);">@ExceptionHandler注解用于处理控制器中抛出的异常，使得开发者可以根据需要灵活地处理异常。同时，使用@ControllerAdvice注解可以将这个异常处理器应用于所有的控制器中。</font>  
<font style="color:rgb(43, 43, 43);">@ExceptionHandler注解是Spring框架中比较常用的注解之一，可以让开发者更加灵活地处理控制器中的异常。</font>  
**<font style="color:rgb(43, 43, 43);">25）@ResponseStatus</font>**  
<font style="color:rgb(43, 43, 43);">作用：用于指定异常的HTTP响应状态码。</font>  
<font style="color:rgb(43, 43, 43);">用例：</font>  
**<font style="color:rgb(43, 43, 43);">26）@ControllerAdvice</font>**  
<font style="color:rgb(43, 43, 43);">作用：用于全局处理异常。</font>  
<font style="color:rgb(43, 43, 43);">@ControllerAdvice是Spring框架中的一个注解，用于定义全局控制器通知。</font>  
<font style="color:rgb(43, 43, 43);">在Spring MVC框架中，控制器通知是一些特殊的组件，它们可以在控制器方法执行前、执行后或抛出异常时执行一些额外的逻辑处理。使用@ControllerAdvice注解可以定义全局控制器通知，它可以应用于所有的控制器。</font>  
<font style="color:rgb(43, 43, 43);">用例：</font>  
<font style="color:rgb(43, 43, 43);">这个类使用@ControllerAdvice注解标注，表示这个类是一个全局控制器通知。在方法级别上，使用@ModelAttribute注解标注方法，表示这个方法会在所有控制器方法执行前执行，用于将当前登录用户信息添加到模型中。</font>  
<font style="color:rgb(43, 43, 43);">使用@InitBinder注解标注方法，表示这个方法会在所有控制器方法执行前执行，用于注册自定义的属性编辑器。</font>  
<font style="color:rgb(43, 43, 43);">使用@ExceptionHandler注解标注方法，表示这个方法会在控制器中抛出异常时执行，用于处理控制器方法中抛出的异常。</font>  
<font style="color:rgb(43, 43, 43);">@ControllerAdvice注解用于定义全局控制器通知，使得开发者可以在所有控制器方法执行前、执行后或抛出异常时执行一些额外的逻辑处理。同时，使用@ModelAttribute注解可以将一些公共的模型数据添加到模型中，使用@InitBinder注解可以注册自定义的属性编辑器，使用@ExceptionHandler注解可以处理控制器方法中抛出的异常。</font>  
<font style="color:rgb(43, 43, 43);">@ControllerAdvice注解是Spring框架中比较常用的注解之一，可以让开发者更加灵活地定义全局控制器通知。</font>  
**<font style="color:rgb(43, 43, 43);">27）@CrossOrigin</font>**  
<font style="color:rgb(43, 43, 43);">作用：用于解决跨域问题。</font>  
<font style="color:rgb(43, 43, 43);">@CrossOrigin是Spring框架中的一个注解，用于解决跨域资源共享（CORS）问题。</font>  
<font style="color:rgb(43, 43, 43);">跨域资源共享是浏览器安全策略的一部分，它限制了浏览器在不同域名之间发送和接收HTTP请求。使用@CrossOrigin注解可以指定允许跨域访问的域名和HTTP方法。</font>  
<font style="color:rgb(43, 43, 43);">用例：</font>  
<font style="color:rgb(43, 43, 43);">这个类使用@RestController注解标注，表示这个类是一个RESTful风格的控制器。在类级别上，使用@RequestMapping注解指定控制器处理的请求路径为/api。同时，使用@CrossOrigin注解可以指定允许跨域访问的域名和HTTP方法。</font>  
<font style="color:rgb(43, 43, 43);">在这个例子中，使用@CrossOrigin注解指定允许来自http://localhost:8080域名的GET和POST请求访问该控制器中的方法。这意味着，在http://localhost:8080域名下的网页可以通过XMLHttpRequest对象发送GET和POST请求，访问该控制器中的方法。</font>  
<font style="color:rgb(43, 43, 43);">@CrossOrigin注解用于解决跨域资源共享（CORS）问题，使得开发者可以更加灵活地控制允许跨域访问的域名和HTTP方法。它是一种简单但非常有效的解决方案，可以使得前端开发者更加轻松地开发跨域应用程序。</font>  
<font style="color:rgb(43, 43, 43);">@CrossOrigin注解是Spring框架中比较常用的注解之一，可以让开发者更加灵活地解决跨域资源共享（CORS）问题。</font>  
**<font style="color:rgb(43, 43, 43);">28）@Async</font>**  
<font style="color:rgb(43, 43, 43);">作用：用于将方法标记为异步执行。</font>  
<font style="color:rgb(43, 43, 43);">在Spring框架中，如果一个方法需要执行一些比较耗时的操作，如果这个方法是在主线程中执行，就会导致主线程被阻塞，用户界面无法响应用户的操作。使用@Async注解可以将这个方法的执行异步化，让主线程继续执行其他任务，提高应用程序的响应性能。</font>  
<font style="color:rgb(43, 43, 43);">用例：</font>  
<font style="color:rgb(43, 43, 43);">这个类使用@Service注解标注，表示这个类是一个服务。在方法级别上，使用@Async注解标注方法，表示这个方法需要异步执行。</font>  
<font style="color:rgb(43, 43, 43);">在这个例子中，getUserDetailsAsync方法使用@Async注解标注，表示这个方法需要异步执行。查询用户信息的操作在异步线程中执行，不会阻塞主线程。同时，这个方法返回一个CompletableFuture对象，表示异步执行的结果。</font>  
<font style="color:rgb(43, 43, 43);">@Async注解用于异步执行方法，可以提高应用程序的响应性能。它是一种简单但非常有效的解决方案，可以使得开发者更加轻松地编写并发应用程序。</font>  
<font style="color:rgb(43, 43, 43);">@Async注解是Spring框架中比较常用的注解之一，可以让开发者更加灵活地异步执行方法。需要注意的是，异步执行的方法必须在一个独立的线程中执行，因此需要使用线程池来管理异步线程的执行。</font>  
**<font style="color:rgb(43, 43, 43);">29）@Cacheable</font>**  
<font style="color:rgb(43, 43, 43);">作用：用于缓存方法的返回值。</font>  
<font style="color:rgb(43, 43, 43);">在Spring框架中，如果一个方法的返回结果是固定的，而且这个方法的执行比较耗时，可以使用@Cacheable注解将这个方法的返回结果缓存起来，下次执行这个方法时直接从缓存中获取结果，避免重复执行。</font>  
<font style="color:rgb(43, 43, 43);">用例：</font>  
<font style="color:rgb(43, 43, 43);">这个类使用@Service注解标注，表示这个类是一个服务。在方法级别上，使用@Cacheable注解标注方法，表示这个方法返回的结果可以被缓存起来。</font>  
<font style="color:rgb(43, 43, 43);">在这个例子中，getUser方法使用@Cacheable注解标注，表示这个方法的返回结果可以被缓存起来。查询用户信息的操作在第一次执行时会被执行，返回结果会被缓存到名为"userCache"的缓存中。下次执行getUser方法时，如果缓存中已经存在这个结果，就直接从缓存中获取结果，不需要再次执行查询操作。</font>  
<font style="color:rgb(43, 43, 43);">@Cacheable注解用于缓存方法的返回结果，可以提高应用程序的执行效率。它是一种简单但非常有效的解决方案，可以使得开发者更加灵活地使用缓存来优化应用程序的性能。</font>  
<font style="color:rgb(43, 43, 43);">@Cacheable注解是Spring框架中比较常用的注解之一，可以让开发者更加轻松地使用缓存来提高应用程序的性能。需要注意的是，使用缓存需要考虑缓存的生命周期和缓存的一致性，必要时需要使用缓存失效机制和缓存更新机制来维护缓存的一致性。</font>  
**<font style="color:rgb(43, 43, 43);">30）@CacheEvict</font>**  
<font style="color:rgb(43, 43, 43);">作用：用于清除缓存。</font>  
<font style="color:rgb(43, 43, 43);">@CacheEvict是Spring框架中的一个注解，用于清空缓存中的数据。</font>  
<font style="color:rgb(43, 43, 43);">在Spring框架中，如果一个方法的执行会导致缓存数据的失效，可以使用@CacheEvict注解将这个方法的缓存数据清空，这样下次执行这个方法时就会重新查询数据并缓存起来。</font>  
<font style="color:rgb(43, 43, 43);">用例：</font>  
<font style="color:rgb(43, 43, 43);">这个类使用@Service注解标注，表示这个类是一个服务。在方法级别上，使用@Cacheable注解标注getUser方法，表示这个方法的返回结果可以被缓存起来。同时，使用@CacheEvict注解标注clearCache方法，表示这个方法会清空名为"userCache"的缓存。</font>  
<font style="color:rgb(43, 43, 43);">在这个例子中，getUser方法使用@Cacheable注解标注，表示这个方法的返回结果可以被缓存起来。查询用户信息的操作在第一次执行时会被执行，返回结果会被缓存到名为"userCache"的缓存中。下次执行getUser方法时，如果缓存中已经存在这个结果，就直接从缓存中获取结果，不需要再次执行查询操作。</font>  
<font style="color:rgb(43, 43, 43);">当调用clearCache方法时，@CacheEvict注解会清空名为"userCache"的缓存，下次执行getUser方法时，就需要重新查询数据并缓存起来。</font>  
<font style="color:rgb(43, 43, 43);">@CacheEvict注解用于清空缓存中的数据，可以使得开发者更加灵活地控制缓存的生命周期和缓存的一致性。它是一种简单但非常有效的解决方案，可以使得开发者更加轻松地使用缓存来提高应用程序的性能。</font>  
<font style="color:rgb(43, 43, 43);">@CacheEvict注解是Spring框架中比较常用的注解之一，可以让开发者更加灵活地控制缓存的生命周期和缓存的一致性。需要注意的是，清空缓存需要谨慎操作，必要时需要考虑缓存的失效机制和缓存更新机制来维护缓存的一致性。</font>  
**<font style="color:rgb(43, 43, 43);">31）@CachePut</font>**  
<font style="color:rgb(43, 43, 43);">作用：用于更新缓存中的数据。</font>  
<font style="color:rgb(43, 43, 43);">@CachePut是Spring框架中的一个注解，用于更新或添加缓存中的数据。</font>  
<font style="color:rgb(43, 43, 43);">在Spring框架中，如果一个方法的执行会导致缓存数据的更新或添加，可以使用@CachePut注解将这个方法的返回结果更新或添加到缓存中。</font>  
<font style="color:rgb(43, 43, 43);">用例：</font>  
<font style="color:rgb(43, 43, 43);">这个类使用@Service注解标注，表示这个类是一个服务。在方法级别上，使用@Cacheable注解标注getUser方法，表示这个方法的返回结果可以被缓存起来。同时，使用@CachePut注解标注updateUser方法，表示这个方法会更新或添加名为"userCache"的缓存。</font>  
<font style="color:rgb(43, 43, 43);">在这个例子中，getUser方法使用@Cacheable注解标注，表示这个方法的返回结果可以被缓存起来。查询用户信息的操作在第一次执行时会被执行，返回结果会被缓存到名为"userCache"的缓存中。下次执行getUser方法时，如果缓存中已经存在这个结果，就直接从缓存中获取结果，不需要再次执行查询操作。</font>  
<font style="color:rgb(43, 43, 43);">当调用updateUser方法时，@CachePut注解会更新或添加名为"userCache"的缓存，下次执行getUser方法时，就可以从缓存中获取更新后的用户信息。</font>  
<font style="color:rgb(43, 43, 43);">@CachePut注解用于更新或添加缓存中的数据，可以使得开发者更加灵活地控制缓存的生命周期和缓存的一致性。它是一种简单但非常有效的解决方案，可以使得开发者更加轻松地使用缓存来提高应用程序的性能。</font>  
<font style="color:rgb(43, 43, 43);">@CachePut注解是Spring框架中比较常用的注解之一，可以让开发者更加灵活地控制缓存的生命周期和缓存的一致性。需要注意的是，更新或添加缓存需要谨慎操作，必要时需要考虑缓存的失效机制和缓存更新机制来维护缓存的一致性。</font>  
**<font style="color:rgb(43, 43, 43);">32）@Transactional</font>**  
<font style="color:rgb(43, 43, 43);">作用：用于启用事务管理功能。</font>  
<font style="color:rgb(43, 43, 43);">@Transactional是Spring框架中的一个注解，用于标识一个方法或类需要使用事务进行操作。</font>  
<font style="color:rgb(43, 43, 43);">在Spring框架中，如果一个方法需要对数据库进行操作，可以使用@Transactional注解来确保这个操作在一个事务中进行，从而保证操作的原子性、一致性、隔离性和持久性。</font>  
<font style="color:rgb(43, 43, 43);">用例：</font>  
<font style="color:rgb(43, 43, 43);">这个类使用@Service注解标注，表示这个类是一个服务。同时，在类级别上使用@Transactional注解标注，表示这个类中的所有方法都需要使用事务进行操作。</font>  
<font style="color:rgb(43, 43, 43);">在这个例子中，createUser和updateUser方法都需要对数据库进行操作，因此使用userRepository来保存或更新用户信息。由于这个类使用了@Transactional注解来标识，因此userRepository的操作都在一个事务中进行，从而保证操作的原子性、一致性、隔离性和持久性。</font>  
<font style="color:rgb(43, 43, 43);">@Transactional注解用于标识一个方法或类需要使用事务进行操作，可以使得开发者更加灵活地控制事务的使用。它是一种简单但非常有效的解决方案，可以使得开发者更加轻松地使用事务来提高应用程序的性能和数据一致性。</font>  
<font style="color:rgb(43, 43, 43);">@Transactional注解是Spring框架中比较常用的注解之一，可以让开发者更加灵活地控制事务的使用。需要注意的是，事务的使用需要谨慎操作，必要时需要考虑事务的隔离级别、超时时间和回滚机制等来维护数据的一致性和应用程序的性能。</font>  
**<font style="color:rgb(43, 43, 43);">34）@EnableAspectJAutoProxy</font>**  
<font style="color:rgb(43, 43, 43);">作用：用于启用AOP功能。</font>  
<font style="color:rgb(43, 43, 43);">@EnableAspectJAutoProxy是Spring框架中的一个注解，用于启用自动代理功能，以便使用AOP（面向切面编程）进行编程。</font>  
<font style="color:rgb(43, 43, 43);">在Spring框架中，如果需要使用AOP来实现某些功能，可以使用@EnableAspectJAutoProxy注解来启用自动代理功能，从而在运行时自动生成代理对象，以便进行切面编程。</font>  
<font style="color:rgb(43, 43, 43);">用例：</font>  
<font style="color:rgb(43, 43, 43);">这个类使用@Configuration注解标注，表示这个类是一个配置类。同时，在类级别上使用@EnableAspectJAutoProxy注解标注，表示这个配置类需要启用自动代理功能。</font>  
<font style="color:rgb(43, 43, 43);">在这个例子中，定义了一个MyAspect类来实现某些功能的切面编程。为了让Spring框架能够自动生成代理对象，需要将MyAspect类加入到Spring容器中，并且使用@Bean注解标注。另外，还定义了一个UserService类来实现某些业务功能。</font>  
<font style="color:rgb(43, 43, 43);">@EnableAspectJAutoProxy注解用于启用自动代理功能，可以使得开发者更加方便地使用AOP来实现某些功能。它是一种简单但非常有效的解决方案，可以让开发者更加轻松地使用切面编程来提高应用程序的性能和可维护性。</font>  
<font style="color:rgb(43, 43, 43);">@EnableAspectJAutoProxy注解是Spring框架中比较常用的注解之一，可以让开发者更加方便地使用AOP来实现某些功能。需要注意的是，AOP的使用需要谨慎操作，必要时需要考虑AOP的切面逻辑、切入点和通知类型等来维护应用程序的性能和可维护性。</font>  
**<font style="color:rgb(43, 43, 43);">35）@Aspect</font>**  
<font style="color:rgb(43, 43, 43);">作用：用于定义切面。</font>  
<font style="color:rgb(43, 43, 43);">@Aspect是Spring框架中的一个注解，用于标识一个类为切面类，从而可以在该类中定义切面逻辑以实现AOP（面向切面编程）。</font>  
<font style="color:rgb(43, 43, 43);">在Spring框架中，如果需要使用AOP来实现某些功能，可以使用@Aspect注解来标识一个类为切面类。在切面类中，可以定义切面逻辑，包括切入点、通知类型和切面顺序等，从而实现AOP编程的功能。</font>  
<font style="color:rgb(43, 43, 43);">用例：</font>  
<font style="color:rgb(43, 43, 43);">这个类使用@Aspect注解标识，表示这个类是一个切面类。同时，还使用@Component注解标识这个类，以便Spring框架能够自动将它加入到Spring容器中。</font>  
<font style="color:rgb(43, 43, 43);">在这个例子中，定义了一个MyAspect类来实现某些功能的切面编程。在这个类中，定义了两个通知类型，即@Before和@After，分别表示在目标方法执行前和执行后执行某些操作。这些通知类型的执行条件是通过切入点表达式来定义的。</font>  
<font style="color:rgb(43, 43, 43);">@Aspect注解用于标识一个类为切面类，可以使得开发者更加方便地使用AOP来实现某些功能。它是一种简单但非常有效的解决方案，可以让开发者更加轻松地使用切面编程来提高应用程序的性能和可维护性。</font>  
<font style="color:rgb(43, 43, 43);">@Aspect注解是Spring框架中比较常用的注解之一，用于标识一个类为切面类。需要注意的是，AOP的使用需要谨慎操作，必要时需要考虑切入点、通知类型和切面顺序等来维护应用程序的性能和可维护性。</font>  
**<font style="color:rgb(43, 43, 43);">36）@Pointcut</font>**  
<font style="color:rgb(43, 43, 43);">作用：用于定义切点。</font>  
<font style="color:rgb(43, 43, 43);">@Pointcut是Spring框架中的一个注解，用于定义一个切入点，从而可以在该切入点上定义通知类型以实现AOP（面向切面编程）。</font>  
<font style="color:rgb(43, 43, 43);">在Spring框架中，如果需要使用AOP来实现某些功能，可以使用@Pointcut注解来定义一个切入点。在切入点上，可以定义切面逻辑，包括通知类型和切面顺序等，从而实现AOP编程的功能。</font>  
<font style="color:rgb(43, 43, 43);">用例：</font>  
<font style="color:rgb(43, 43, 43);">这个类使用@Aspect注解标识，表示这个类是一个切面类。同时，还使用@Component注解标识这个类，以便Spring框架能够自动将它加入到Spring容器中。</font>  
<font style="color:rgb(43, 43, 43);">在这个例子中，定义了一个MyAspect类来实现某些功能的切面编程。在这个类中，使用@Pointcut注解定义了一个切入点，即userServicePointcut()方法。在这个切入点上，定义了两个通知类型，即@Before和@After，分别表示在目标方法执行前和执行后执行某些操作。</font>  
<font style="color:rgb(43, 43, 43);">@Pointcut注解用于定义一个切入点，可以使得开发者更加方便地使用AOP来实现某些功能。它是一种简单但非常有效的解决方案，可以让开发者更加轻松地使用切面编程来提高应用程序的性能和可维护性。</font>  
<font style="color:rgb(43, 43, 43);">@Pointcut注解是Spring框架中比较常用的注解之一，用于定义一个切入点。需要注意的是，AOP的使用需要谨慎操作，必要时需要考虑切入点、通知类型和切面顺序等来维护应用程序的性能和可维护性。</font>  
**<font style="color:rgb(43, 43, 43);">37）@Before</font>**  
<font style="color:rgb(43, 43, 43);">作用：用于在方法执行前执行通知。</font>  
<font style="color:rgb(43, 43, 43);">@Before是Spring框架中的一个注解，用于定义在目标方法执行前执行的通知类型，以实现AOP（面向切面编程）。</font>  
<font style="color:rgb(43, 43, 43);">在Spring框架中，如果需要在目标方法执行前执行某些操作，可以使用@Before注解来定义一个通知类型。在这个通知类型中，可以编写自己的逻辑代码，从而实现AOP编程的功能。</font>  
<font style="color:rgb(43, 43, 43);">用例：</font>  
**<font style="color:rgb(43, 43, 43);">38）@After</font>**  
<font style="color:rgb(43, 43, 43);">作用：用于在方法执行后执行通知。</font>  
<font style="color:rgb(43, 43, 43);">@After是Spring框架中的一个注解，用于定义在目标方法执行后执行的通知类型，以实现AOP（面向切面编程）。</font>  
<font style="color:rgb(43, 43, 43);">在Spring框架中，如果需要在目标方法执行后执行某些操作，可以使用@After注解来定义一个通知类型。在这个通知类型中，可以编写自己的逻辑代码，从而实现AOP编程的功能。</font>  
<font style="color:rgb(43, 43, 43);">用例：</font>  
**<font style="color:rgb(43, 43, 43);">39）@Around</font>**  
<font style="color:rgb(43, 43, 43);">作用：用于在方法执行前后执行通知。</font>  
<font style="color:rgb(43, 43, 43);">@Around是Spring框架中的一个注解，用于定义在目标方法执行前后执行的通知类型，以实现AOP（面向切面编程）。</font>  
<font style="color:rgb(43, 43, 43);">在Spring框架中，如果需要在目标方法执行前后执行某些操作，可以使用@Around注解来定义一个通知类型。在这个通知类型中，可以编写自己的逻辑代码，从而实现AOP编程的功能。</font>  
<font style="color:rgb(43, 43, 43);">用例：</font>  
**<font style="color:rgb(43, 43, 43);">40）@AfterReturning</font>**  
<font style="color:rgb(43, 43, 43);">作用：用于在方法返回结果后执行通知。</font>  
<font style="color:rgb(43, 43, 43);">@AfterReturning是Spring框架中的一个注解，用于定义在目标方法返回结果后执行的通知类型，以实现AOP（面向切面编程）。</font>  
<font style="color:rgb(43, 43, 43);">在Spring框架中，如果需要在目标方法返回结果后执行某些操作，可以使用@AfterReturning注解来定义一个通知类型。在这个通知类型中，可以编写自己的逻辑代码，从而实现AOP编程的功能。</font>  
<font style="color:rgb(43, 43, 43);">用例：</font>  
**<font style="color:rgb(43, 43, 43);">41）@AfterThrowing</font>**  
<font style="color:rgb(43, 43, 43);">作用：用于在方法抛出异常后执行通知。</font>  
<font style="color:rgb(43, 43, 43);">@AfterThrowing是Spring框架中的一个注解，用于定义在目标方法抛出异常后执行的通知类型，以实现AOP（面向切面编程）。</font>  
<font style="color:rgb(43, 43, 43);">在Spring框架中，如果需要在目标方法抛出异常后执行某些操作，可以使用@AfterThrowing注解来定义一个通知类型。在这个通知类型中，可以编写自己的逻辑代码，从而实现AOP编程的功能。</font>  
<font style="color:rgb(43, 43, 43);">用例：</font>  
**<font style="color:rgb(43, 43, 43);">42）@Order</font>**  
<font style="color:rgb(43, 43, 43);">作用：用于指定切面的执行顺序。</font>  
<font style="color:rgb(43, 43, 43);">@Order是Spring框架中的一个注解，用于定义切面的执行顺序。</font>  
<font style="color:rgb(43, 43, 43);">在Spring框架中，如果有多个切面类需要对同一个方法进行切面处理，那么这些切面类的执行顺序可能会影响到最终的结果。为了控制这些切面类的执行顺序，可以使用@Order注解来定义它们的执行顺序。</font>  
<font style="color:rgb(43, 43, 43);">@Order注解可以应用在切面类上，用于指定切面执行的顺序。它的参数为一个整数，数值越小表示优先级越高，数值相同时按照类名的自然顺序进行排序。</font>  
<font style="color:rgb(43, 43, 43);">用例：</font>  
**<font style="color:rgb(43, 43, 43);">43）@Slf4j</font>**  
<font style="color:rgb(43, 43, 43);">作用：用于简化日志记录。</font>  
<font style="color:rgb(43, 43, 43);">@Slf4j是Lombok框架中的一个注解，用于在Java类中自动生成日志记录器。</font>  
<font style="color:rgb(43, 43, 43);">在Java开发中，日志记录是非常重要的一环，可以更好地了解程序的运行情况，从而更好地进行调试和优化。通常情况下，需要手动引入日志框架（如Log4j、SLF4J等）并编写相应的日志记录代码。这些代码可能会比较繁琐，而且容易出现错误。为了简化这个过程，Lombok框架提供了一个@Slf4j注解，可以在Java类中自动生成日志记录器。</font>  
<font style="color:rgb(43, 43, 43);">使用@Slf4j注解非常简单，只需要在Java类中添加这个注解即可。在使用时，可以直接使用log变量来记录日志，而不需要再引入其他的日志框架</font>  
<font style="color:rgb(43, 43, 43);">用例：</font>  
<font style="color:rgb(43, 43, 43);">在这个例子中，定义了一个MyService类，并使用@Slf4j注解来自动生成日志记录器。然后，在doSomething()方法中，直接使用log变量来记录日志，而不需要再引入其他的日志框架。</font>  
<font style="color:rgb(43, 43, 43);">需要注意的是，使用@Slf4j注解需要在编译器中安装Lombok插件，否则可能会出现编译错误。另外，虽然@Slf4j注解非常方便，但在实际应用中，还需要根据实际情况选择合适的日志框架，并编写相应的日志记录代码。</font>  
<font style="color:rgb(43, 43, 43);">总之，@Slf4j是Lombok框架中的一个注解，可以在Java类中自动生成日志记录器，从而简化日志记录的过程。它是一种极为方便的解决方案，可以提高应用程序的可维护性和可读性。</font>  
**<font style="color:rgb(43, 43, 43);">44）@Data</font>**  
<font style="color:rgb(43, 43, 43);">作用：用于自动生成JavaBean的getters、setters、toString、hashCode和equals方法。</font>  
<font style="color:rgb(43, 43, 43);">@Data是Lombok框架中的一个注解，可以自动生成Java类的getter、setter、equals、hashCode和toString等方法。</font>  
<font style="color:rgb(43, 43, 43);">在Java开发中，经常需要编写一些POJO类来表示数据结构。这些类通常包含一些成员变量，并且需要编写相应的getter、setter、equals、hashCode和toString等方法。这些方法通常是相似的，而且比较繁琐。为了简化这个过程，Lombok框架提供了一个@Data注解，可以自动生成这些方法。</font>  
<font style="color:rgb(43, 43, 43);">使用@Data注解非常简单，只需要在Java类上添加这个注解即可。在使用时，可以直接访问类的成员变量，并且可以自动生成相应的getter、setter、equals、hashCode和toString等方法。</font>  
<font style="color:rgb(43, 43, 43);">用例：</font>  
**<font style="color:rgb(43, 43, 43);">45）@NoArgsConstructor</font>**  
<font style="color:rgb(43, 43, 43);">作用：用于生成无参构造函数。</font>  
<font style="color:rgb(43, 43, 43);">@NoArgsConstructor是Lombok框架中的一个注解，用于自动生成一个无参构造方法。</font>  
<font style="color:rgb(43, 43, 43);">在Java开发中，经常需要编写一些POJO类来表示数据结构。这些类通常包含一些成员变量，并且需要编写相应的构造方法。在某些情况下，可能需要编写一个无参构造方法，用于创建一个对象的实例。这个构造方法通常是简单的、无需参数的。为了简化这个过程，Lombok框架提供了一个@NoArgsConstructor注解，可以自动生成一个无参构造方法。</font>  
<font style="color:rgb(43, 43, 43);">使用@NoArgsConstructor注解非常简单，只需要在Java类上添加这个注解即可。在使用时，可以直接创建对象的实例，而不需要手动编写无参构造方法。</font>  
<font style="color:rgb(43, 43, 43);">用例：</font>  
<font style="color:rgb(43, 43, 43);">在这个例子中，定义了一个User类，并使用@NoArgsConstructor注解来自动生成一个无参构造方法。然后，在其他的Java类中，可以直接创建User对象的实例，而不需要手动编写无参构造方法。</font>  
<font style="color:rgb(43, 43, 43);">需要注意的是，使用@NoArgsConstructor注解需要在编译器中安装Lombok插件，否则可能会出现编译错误。另外，虽然@NoArgsConstructor注解非常方便，但在实际应用中，还需要根据实际情况选择合适的构造方法，并编写相应的代码。</font>  
<font style="color:rgb(43, 43, 43);">总之，@NoArgsConstructor是Lombok框架中的一个注解，用于自动生成一个无参构造方法，从而简化Java开发的过程。它是一种极为方便的解决方案，可以提高应用程序的可维护性和可读性。</font>  
**<font style="color:rgb(43, 43, 43);">46）@AllArgsConstructor</font>**  
<font style="color:rgb(43, 43, 43);">作用：用于生成全参构造函数。</font>  
<font style="color:rgb(43, 43, 43);">@AllArgsConstructor是Lombok框架中的一个注解，用于自动生成一个全参构造方法。</font>  
<font style="color:rgb(43, 43, 43);">在Java开发中，经常需要编写一些POJO类来表示数据结构。这些类通常包含一些成员变量，并且需要编写相应的构造方法。在某些情况下，可能需要编写一个全参构造方法，用于初始化所有成员变量。这个构造方法通常包含所有成员变量作为参数。为了简化这个过程，Lombok框架提供了一个@AllArgsConstructor注解，可以自动生成一个全参构造方法。</font>  
<font style="color:rgb(43, 43, 43);">使用@AllArgsConstructor注解非常简单，只需要在Java类上添加这个注解即可。在使用时，可以直接创建对象的实例，并传入相应的参数，而不需要手动编写全参构造方法。</font>  
<font style="color:rgb(43, 43, 43);">用例：</font>  
<font style="color:rgb(43, 43, 43);">在这个例子中，定义了一个User类，并使用@AllArgsConstructor注解来自动生成一个全参构造方法。然后，在其他的Java类中，可以直接创建User对象的实例，并传入相应的参数，而不需要手动编写全参构造方法。</font>  
<font style="color:rgb(43, 43, 43);">需要注意的是，使用@AllArgsConstructor注解需要在编译器中安装Lombok插件，否则可能会出现编译错误。另外，虽然@AllArgsConstructor注解非常方便，但在实际应用中，还需要根据实际情况选择合适的构造方法，并编写相应的代码。</font>  
<font style="color:rgb(43, 43, 43);">总之，@AllArgsConstructor是Lombok框架中的一个注解，用于自动生成一个全参构造方法，从而简化Java开发的过程。它是一种极为方便的解决方案，可以提高应用程序的可维护性和可读性。</font>  
**<font style="color:rgb(43, 43, 43);">47）@Builder</font>**  
<font style="color:rgb(43, 43, 43);">作用：用于生成Builder模式的构造函数。</font>  
<font style="color:rgb(43, 43, 43);">@Builder是Lombok框架中的一个注解，用于自动生成一个Builder模式的构造器。</font>  
<font style="color:rgb(43, 43, 43);">在Java开发中，经常需要编写一些POJO类来表示数据结构。这些类通常包含一些成员变量，并且需要编写相应的构造方法。在某些情况下，可能需要编写一个Builder模式的构造器，用于方便地创建对象实例。Builder模式是一种创建对象的设计模式，它可以通过链式调用的方式设置对象的属性，并最终创建一个不可变的对象。为了简化这个过程，Lombok框架提供了一个@Builder注解，可以自动生成一个Builder模式的构造器。</font>  
<font style="color:rgb(43, 43, 43);">使用@Builder注解非常简单，只需要在Java类上添加这个注解即可。在使用时，可以使用链式调用的方式设置对象的属性，并最终创建一个不可变的对象。</font>  
<font style="color:rgb(43, 43, 43);">用例：</font>  
<font style="color:rgb(43, 43, 43);">在这个例子中，定义了一个User类，并使用@Builder注解来自动生成一个Builder模式的构造器。然后，在其他的Java类中，可以使用链式调用的方式设置User对象的属性，并最终创建一个不可变的对象。</font>  
<font style="color:rgb(43, 43, 43);">需要注意的是，使用@Builder注解需要在编译器中安装Lombok插件，否则可能会出现编译错误。另外，虽然@Builder注解非常方便，但在实际应用中，还需要根据实际情况选择合适的构造方法，并编写相应的代码。</font>  
<font style="color:rgb(43, 43, 43);">总之，@Builder是Lombok框架中的一个注解，用于自动生成一个Builder模式的构造器，从而简化Java开发的过程。它是一种极为方便的解决方案，可以提高应用程序的可维护性和可读性。</font>  
**<font style="color:rgb(43, 43, 43);">48）@EqualsAndHashCode</font>**  
<font style="color:rgb(43, 43, 43);">作用：用于生成hashCode和equals方法。</font>  
<font style="color:rgb(43, 43, 43);">@EqualsAndHashCode是Lombok框架中的一个注解，用于自动生成equals()和hashCode()方法。</font>  
<font style="color:rgb(43, 43, 43);">在Java开发中，经常需要比较两个对象是否相等，并且需要根据对象的属性生成一个hashCode值。为了简化这个过程，Lombok框架提供了一个@EqualsAndHashCode注解，可以自动生成equals()和hashCode()方法。</font>  
<font style="color:rgb(43, 43, 43);">使用@EqualsAndHashCode注解非常简单，只需要在Java类上添加这个注解即可。在使用时，Lombok会根据类的属性自动生成equals()和hashCode()方法。如果两个对象的所有属性都相等，那么它们的equals()方法返回true，并且它们的hashCode()方法返回相同的值。</font>  
<font style="color:rgb(43, 43, 43);">用例：</font>  


```java
@EqualsAndHashCode
publicclassUser{
    privateLongid;
    privateStringname;
    privateIntegerage;
}
```



**<font style="color:rgb(43, 43, 43);">49）</font>****<font style="color:rgb(43, 43, 43);">@ToString</font>**  
<font style="color:rgb(43, 43, 43);">作用：用于生成toString方法。</font>  
<font style="color:rgb(43, 43, 43);">@ToString</font><font style="color:rgb(43, 43, 43);">是Lombok框架中的一个注解，用于自动生成</font><font style="color:rgb(43, 43, 43);">toString()</font><font style="color:rgb(43, 43, 43);">方法。</font>  
<font style="color:rgb(43, 43, 43);">在Java开发中，经常需要将对象转换为字符串，以便于输出或日志记录。为了简化这个过程，Lombok框架提供了一个</font><font style="color:rgb(43, 43, 43);">@ToString</font><font style="color:rgb(43, 43, 43);">注解，可以自动生成</font><font style="color:rgb(43, 43, 43);">toString()</font><font style="color:rgb(43, 43, 43);">方法。</font>  
<font style="color:rgb(43, 43, 43);">使用</font><font style="color:rgb(43, 43, 43);">@ToString</font><font style="color:rgb(43, 43, 43);">注解非常简单，只需要在Java类上添加这个注解即可。在使用时，Lombok会根据类的属性自动生成</font><font style="color:rgb(43, 43, 43);">toString()</font><font style="color:rgb(43, 43, 43);">方法，这个方法将输出类的名称和所有属性的名称和值。如果需要排除某些属性，可以使用</font><font style="color:rgb(43, 43, 43);">exclude</font><font style="color:rgb(43, 43, 43);">属性来指定排除的属性。</font>  
<font style="color:rgb(43, 43, 43);">用例：</font>  




<font style="color:rgb(108, 108, 108);">1</font>



```java
@ToString(exclude="password")
publicclassUser{
    privateLongid;
    privateStringname;
    privateStringpassword;
}
```

<font style="color:rgb(108, 108, 108);">2</font>

<font style="color:rgb(108, 108, 108);">3</font>

<font style="color:rgb(108, 108, 108);">4</font>

<font style="color:rgb(108, 108, 108);">5</font>

<font style="color:rgb(108, 108, 108);">6</font>



**<font style="color:rgb(43, 43, 43);">50）</font>****<font style="color:rgb(43, 43, 43);">@Getter</font>**  
<font style="color:rgb(43, 43, 43);">作用：用于生成getters方法。</font>  
<font style="color:rgb(43, 43, 43);">@Getter</font><font style="color:rgb(43, 43, 43);">是Lombok框架中的一个注解，用于自动生成getter方法。</font>  
<font style="color:rgb(43, 43, 43);">在Java开发中，经常需要为类的属性编写getter和setter方法。为了简化这个过程，Lombok框架提供了一个</font><font style="color:rgb(43, 43, 43);">@Getter</font><font style="color:rgb(43, 43, 43);">注解，可以自动生成getter方法。</font>  
<font style="color:rgb(43, 43, 43);">使用</font><font style="color:rgb(43, 43, 43);">@Getter</font><font style="color:rgb(43, 43, 43);">注解非常简单，只需要在Java类上添加这个注解即可。在使用时，Lombok会根据类的属性自动生成对应的getter方法。如果需要生成setter方法，可以使用</font><font style="color:rgb(43, 43, 43);">@Setter</font><font style="color:rgb(43, 43, 43);">注解。</font>  
<font style="color:rgb(43, 43, 43);">用例：</font>  


<font style="color:rgb(108, 108, 108);">1</font>



```java
@Getter
publicclassUser{
    privateLongid;
    privateStringname;
    privateIntegerage;
}
```

<font style="color:rgb(108, 108, 108);"></font>

<font style="color:rgba(140, 140, 140, 0.5);background-color:rgb(245, 245, 245);"></font>

<font style="color:rgb(108, 108, 108);">1</font>

<font style="color:rgb(108, 108, 108);">2</font>

<font style="color:rgb(108, 108, 108);">3</font>

<font style="color:rgb(108, 108, 108);">4</font>



  
 



> 更新: 2025-04-20 22:38:57  
> 原文: <https://www.yuque.com/aaron-wecc3/dhluml/ygu9n7gbwctqhsut>