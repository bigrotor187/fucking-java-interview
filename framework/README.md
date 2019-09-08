|[Spring](https://github.com/bigrotor187/awesome-java-interview/tree/master/framework#spring)|[SpringMVC](https://github.com/bigrotor187/awesome-java-interview/tree/master/framework#springmvc)|[Mybatis](https://github.com/bigrotor187/awesome-java-interview/tree/master/framework#mybatis)|[SpringBoot](https://github.com/bigrotor187/awesome-java-interview/tree/master/framework#springboot)|[Hibernate](https://github.com/bigrotor187/awesome-java-interview/tree/master/framework#hibernate)|[Redis](https://github.com/bigrotor187/awesome-java-interview/tree/master/framework#redis)|
|------|---------|-------|----------|---------|------|

# Spring

## Spring Framework

- [1、Spring 是如何简化 Java 开发的？]()
- [2、什么是 Spring Framework？]()
- [3、Spring Framework 有哪些优点？]()
- [4、Spring 有哪些子项目吗？请简要描述。]()
- [5、Spring 框架中用到了哪些设计模式？请举例说明。]()
- [6、Spring 有哪些最佳实践？]()

### **1、Spring 是如何简化 Java 开发的？**

为了降低 Java 开发的复杂性，Spring 采取了以下 4 种关键策略：
  - 基于 POJO 的轻量级和最小侵入性编程；
  - 通过依赖注入和面向接口实现松耦合；
  - 基于切面和惯例进行声明式编程；
  - 通过切面和模板减少样板式代码。
  
### **2、什么是 Spring Framework？**

Spring 是一个开源框架，Spring 诞生之初的主要目的是作为 EJB 的轻量级替代品，旨在降低应用程序开发的复杂度。它增强了 POJO，使之具备了之前只有 EJB 和其他企业级 Java 规范才具有的功能。
  - Spring 是轻量级、松散耦合的。
    > 它的轻量级主要是相对于 EJB 而言。但是随着 Spring 体系越来越庞大，添加 Spring 的依赖管理越来越耗时，写配置挤占了写应用程序逻辑的时间，所以后来推出了 Spring Boot。
  - Spring 具有分层体系结构，允许用户选择组件，同时为 J2EE 应用程序开发提供了一个有凝聚力的框架。
  - Spring 可以继承其他框架，如 Spring MVC、Hibernate、Mybatis 等，所以又被称为框架饿的框架（粘合剂、脚手架）

### **3、Spring Framework 有哪些优点？**
- 轻量级：在开发中使用框架会有一点点开销，但不会像重量级的 EJB 一样
- 控制反转（IOC）：也叫依赖注入，Spring 容器负责处理各种对象的依赖关系，而不是创建或查找依赖对象
- 面向切面编程（AOP）：Spring 支持 AOP 将业务逻辑与系统服务分开
- IOC 容器：它管理 Spring Bean 生命周期和项目特定配置
- MCV 框架（Spring Mvc）：用于创建 Web 应用程序或 RESTful Web 服务，能够返回 XML / JSON 响应
- 事务管理：通过使用 Java 注解或 Spring Bean XML 配置文件，减少 JDBC　操作和文件上传等的样板代码量，适程序更加简洁
- 异常处理：Spring 提供了一个方便的 API，用于将特定技术的异常转换为非检查型的异常
  
### **4、Spring 有哪些子项目吗？请简要描述。**
- Core：提供 Spring 框架核心基础部分的关键模块，比如 Ioc 或 DI
- JDBC：此模块启用 JDBC 抽象层，无需对特定供应商数据库执行 JDBC 编码
- ORM 集成：为流行的对象映射 API 提供集成，例如 JPA、JDO、Hibernate、Mybatis 等
- Web：面向 Web 的集成模块，提供多部分文件上载，Servlet 监听器和面向 Web 的应用程序上下文功能
- MVC framework：一个实现了模型-视图-控制设计模式的 Web 模块
- AOP 模块：面向切面编程的实现允许定义更加简洁的方法-拦截器和切入点

![]()
  
### **5、Spring 框架中用到了哪些设计模式？请举例说明。**

- 代理模式（Proxy Pattern） — 在 AOP 和 remoting 中被用的比较多。
- 单例模式（Singleton Pattern） — 在 Spring 配置文件中定义的 Bean 默认为单例模式。
- 模板方法（Template Method Pattern） —用来解决代码重复的问题。如 RestTemplate、JmsTemplate、JdbcTemplate 。
- 前端控制器（Front Controller） — Spring提供了 DispatcherServlet 来对请求进行分发。
- 视图帮助(View Helper) — Spring 提供了一系列的 JSP 标签，高效宏来辅助将分散的代码整合在视图里。
- 依赖注入（Dependency Injection） — 贯穿于 BeanFactory / ApplicationContext 接口的核心理念。
- 工厂模式（Factory Pattern） — BeanFactory 用来创建对象的实例。
- 适配器模式（Adapter Pattern） — 主要在 Spring Web 和 Spring MVC 模块应用。
<br>

> 更多详情请参考: <br>
  （1）[Spring 框架中的设计模式（一）](http://www.iocoder.cn/Spring/DesignPattern-1/)<br>
  （2）[Spring 框架中的设计模式（二）](http://www.iocoder.cn/Spring/DesignPattern-2/)<br>
  （3）[Spring 框架中的设计模式（三）](http://www.iocoder.cn/Spring/DesignPattern-3/)<br>
  （4）[Spring 框架中的设计模式（四）](http://www.iocoder.cn/Spring/DesignPattern-4/)<br>
  （5）[Spring 框架中的设计模式（五）](http://www.iocoder.cn/Spring/DesignPattern-5/)
    
### **6、Spring 有哪些最佳实践？**

- 为组件使用正确的注解可以一目了然当前层的作用。比如，对于控制层，使用 @Controller，对于业务层，使用 @Service， 对于 DAO 层使用 @Repository。
- 可以根据具体用途划分 Spring Bean，如 spring-jdbc.xml, spring-security.xml 等。
- 尽可能地配置 bean 依赖项，尽量避免自动装配。
- 对于应用程序级的属性，最好的方法是创建属性文件并在 Spring Bean 的配置文件中读取它。
<br>

> 更多详情请参考：[spring-best-practices](https://www.journaldev.com/2696/spring-interview-questions-and-answers#spring-best-practices)


## Spring Bean
- [1、什么是 Spring Bean？]()
- [2、Spring Bean 配置文件的重要性是什么？]()
- [3、Spring Bean 有哪些配置方式？]()
- [4、Spring Bean 支持哪几种 Bean Scope？]()
- [5、Spring Bean 的生命周期是什么样的？]()
- [6、Spring 中单例 Bean 是线程安全的吗？]()
- [7、Spring Bean 是否提供线程安全性？]()
- [8、Spring 有哪些依赖注入的方式？或者说 Spring 是如何注入 bean 的？]()
- [9、Spring Bean 定义是如何生成的？]()
- [10、Spring Bean 定义是如何注册的？]()

### **1、什么是 Spring Bean？**
- Spring Bean 是由 Spring IoC 容器初始化的 Java 对象。 
- Spring Bean 由 Spring IoC 容器实例化，配置，装配和管理。
- Spring Bean 基于用户提供给 IoC 容器的配置元数据 Bean Definition 创建。

### **2、Spring Bean 配置文件的重要性是什么？**
- 当使用 Spring Bean 配置文件来定义将由 Spring Context 初始化的所有 Bean 时，在创建  Spring ApplicationContext 实例时，会去读取  spring bean XML 配置文件并初始化这些文件
- 初始化上下文后，可以通过它获取不同的 Bean 实例
- 除了 Spring Bean 的配置之外，该文件还包含 Spring MVC 拦截器，视图解析器以及其他元素，以支持基于注解的配置

### **3、Spring Bean 有哪些配置方式？**
- XML 配置
- Java Config 配置
- 注解配置
### **4、Spring Bean 支持哪几种 Bean Scope？**
- Singleton
- Prototype
- Request
- Session
- Application
# **5、Spring Bean 的生命周期是什么样的？**
- 首先，需要基于Java或XML bean定义来实例化Spring bean。可能还需要执行一些初始化以使其进入可用状态。
- 之后，当不再需要bean时，它将从IoC容器中删除。

![](https://github.com/bigrotor187/awesome-java-interview/blob/master/img/Spring%20Framework.jpg)

### **6、Spring 中单例 Bean 是线程安全的吗？**
- Spring 中单例 Bean 不是线程安全的，因为线程安全是关于执行的，而单例则是一种专注于创建的设计模式
- 线程安全仅仅取决于 bean 本身的实现
- Spring 使用 ThreadLocal 解决线程安全问题，“以空间换时间”的方式为每一个线程都提供了一份变量，因此可以同时访问而互不影响。
> 更多详情请参考：<br>
> （1）[Spring单例与线程安全小结](https://www.cnblogs.com/doit8791/p/4093808.html) <br>
> （2）[聊一聊Spring中的线程安全性](https://juejin.im/post/5a0045ef5188254de169968e#heading-0)
  
### **7、Spring Bean 是否提供线程安全性？**

- Spring 并没有保证对象的线程安全，需要由开发者自己编写解决线程安全问题的代码。
- Spring 对每个 bean 提供了一个 scope 属性来表示该 bean 的作用域，其中默认的 scope 是 singleton，因此每个上下文只有一个实例。这意味所有线程都共享一个单例实例 Bean，因此存在资源竞争，可能会导致数据不一致。因此，在默认模式下，spring bean不是线程安全的。
- 可以将 Spring Bean 的 scope 从 singleton 修改为 request, prototype or session 来获得线程安全，但是会牺牲一部分性能。

### **8、Spring 有哪些依赖注入的方式？或者说 Spring 是如何注入 bean 的？**

- setter注入
- 构造器注入
- 接口注入


### **9、Spring Bean 定义是如何生成的？**
- bean 定义表示对一个类的描述，所以要先生成 bean 定义，然后把它注册到容器中。
- bean 定义的生成主要有两种方式，一种是基于类本身，如知道了类名或类的 class。还有一种是不知道类本身的信息，但是知道它是由一个其他类的工厂方法返回的。而工厂方法又分为静态的和非静态的，所以我们只能记录下这些工厂方法信息到 bean 定义中，在运行时调用工厂方法，获取 bean 的实例对象。
- 工厂方法这种应用场景不多，所以实际上很少用。
  
### **10、Spring Bean 定义是如何注册的？**
- 使用注解注册 bean 定义
  - 标有 @Component 注解的类
  - 标有 @Configuration 注解的类
  - 标有 @Configuration 注解的类里标有 @Bean 注解的方法返回的类

  > PS：这种方式可以用于业务类的注册，也可以用于 Spring 框架内部的类注册。优点是简单方便，缺点是不够灵活，很难根据一个条件判断来注册不同的 bean 定义。
- 使用 XML 配置注册 bean 定义
  - 在标有 @Configuration 注解的类上，使用 @ImportResource 注解引入 XML 配置文件

  > PS：这种方式是在注解里也能使用 XML。建议是尽量不用，优先使用注解的方式，除非是是在历史遗留的系统中。

- 使用 @Import 注解引入
  - 在标有 @Configuration 注解的类上，使用 @Import 注解引入其他标有 @Configuration 注解的类

  > PS：这种方式仅用于没有类路径扫描功能的代码，现在大都基于 SpringBoot，所以这种方式现在很少用了。

- 使用 ImportSelector 接口注册 bean 定义
```java
  public interface ImportSelector {
    String[] selectImports(AnnotationMetadata importingClassMetadata);
  }
```

  > PS：<br>
  （1）接口方法返回的是类名称的数组，这些类将会被注册 bean 定义。<br>
  （2）在实现这个接口时，可以根据不同的情况返回不同的类名称，这就非常的灵活，实现了动态注册 bean 定义的需求。

- 使用 ImportBeanDefinitionRegistrar 接口注册 bean 定义
 ```java
  public interface ImportBeanDefinitionRegistrar {
    void registerBeanDefinitions(AnnotationMetadata importingClassMetadata, BeanDefinitionRegistry registry);
  }
 ```

 > PS：这个接口没有返回值，所以需要自己写代码直接注册 bean 定义，当然也是非常灵活的。在用法上和上面方法一样，包括接口方法参数的含义也一样。

- 使用 BeanDefinitionRegistryPostProcessor 接口注册 bean 定义

```java
  public interface BeanDefinitionRegistryPostProcessor extends BeanFactoryPostProcessor {
     void postProcessBeanDefinitionRegistry(BeanDefinitionRegistry registry) throws BeanException;
  }
```

> PS：<br>
（1）`BeanDefinitionRegistryPostProcessor`接口专门为其他类注册 `bean` 定义，通过 `postProcessBeanDefinitionRegistry` 方法来实现；<br>
（2）`BeanDefinitionRegistryPostProcessor`接口有一个非常重要的实现类 `ConfigurationClassPostProcessor`，里面包含了所有 Spring 支持的注册 `bean` 定义方式的实现。<br>
（3）Spring 统一了编程模型，所以 `ConfigurationClassPostProcessor` 类也被注册了 `bean` 定义。

更多详情请参考：[品Spring：bean定义上梁山](https://mp.weixin.qq.com/s/FDtjJrPMgciM_W7vUpNVbg)

## Spring IoC

### **1、什么是 Spring IoC 框架？**
### **2、什么是依赖注入？**
### **3、IoC 和 DI 有什么区别？**
### **4、Spring 中有哪几种容器？**
### **5、Spring 有哪些常用的 BeanFactory 容器？请简要介绍一下。**
### **6、Spring 有哪些常用的 ApplicationContext 容器？请简要介绍一下。**
### **7、Spring IoC 有什么好处/优点？**
### **8、请简述 Spring IoC 的实现机制。**
### **9、Spring IoC 中有哪些不同类型的事件？**
### **10、Spring 中哪种注入 bean 的方式是最好的？为什么？**
### **11、BeanFactory 和 Application 两种容器有什么区别？**

## Spring 注解

### **1、什么是基于注解的容器配置？**
### **2、@Component、@Controller、@Repository、@Service 之间有什么区别？**
### **3、@RequestMapping 注解是如何工作的？**
### **4、@Required 注解有什么用？**
### **5、@Autowired 注解有什么用？**
### **6、@Qualifier 注解有什么而用？**

## Spring AOP



## Spring 事务



# SpringMVC

# Mybatis

# SpringBoot

# Hibernate

# Redis
