# spring基础

1. 项目生成地址:https://start.spring.io/
2. 查看spring的bean:http://localhost:8080/actuator/beans
3. 健康监测:http://localhost:8080/actuator/health

## 发现

1. lombok:减少代码

# Spring 中的数据操作

##　单数据源配置

springboot配置数据库驱动后,对应的事务,DataSourceAutoConfiguration,JdbcTemplate会自动配置





## 多数据源配置

排除Spring Boot的自动配置

* DataSourceAutoConfiguration

* DataSourceTransactionManagerAutoConfiguration

* JdbcTemplateAutoConfiguration

## 连接池
1. HikariCP

2. Alibaba Druid

## jdbc操作

## 了解 Spring 的抽象

### 事务抽象

## actuator

health

beans

mappings

env



# AOP

## 解决问题

oop面向对象,将任务模块化分解,横向切分,但是针对以每个模块的通用功能做同意的处理,需要在每一个模块做处理(例如:日志),出现了代码混乱和代码分散等问题.

所以,为了解决这个问题,针对以整体模块,纵向处理代码,切面处理

## 优势劣势

### 优势

把次要问题代码放在一个统一的地方，而不是在基本业务逻辑中

### 劣势

aop不能独立,需要"寄生"在oop系统中

## 适用场景

Authentication 权限

Caching 缓存

Context passing 内容传递

Error handling 错误处理

Lazy loading　懒加载

Debugging　　调试

logging, tracing, profiling and monitoring　记录跟踪　优化　校准

Performance optimization　性能优化

Persistence　　持久化

Resource pooling　资源池

Synchronization　同步

Transactions 事务

## 组成部分

### aop历史

* 静态aop
  * 代表:aspectJ
  * 预先编译到系统中:aspectJ使用ajc编辑器将各个aspect以java字节码的形式编译到系统静态类中
  * 优点:虚拟机直接加载java类就行,运行速度快
  * 缺点:灵活性不够,改变织入位置,重新修改Aspect定义文件
* 动态aop
  * 例如:spring aop,AspectJ融合AspectWerkez框架
  * 系统运行之后织入
  * 优点:配置方便:xml/注解
  * 缺点:性能损失(可容忍)

### 专业术语

* Joinpoint **连接点**
  * 方法调用点
* Pointcut **切入点**
  * 将多个Joinpoint集中起来的规则
* Advice **通知**
  * (多个方法调用的统一执行点)定义了在 pointcut 里面定义的程序点具体要做的操作
  * 场景:有两种规则的多个位置,需要做同一种操作
* **introduction引介**
* Aspect **切面**:
  * 是切入点和通知的结合
* **weaving织入**
  * 入是一个过程，是将切面应用到目标对象从而创建出AOP代理对象的过程，织入可以在编译期，类装载期，运行期进行。
* AOL aop
  * 实现语言的统称
* 织入和织入器
  * ​	AOP集成到OOP系统中

## 底层原理

### Java平台实现机制

- 动态代理
  - 针对于接口
  - spring aop,Nanning用此种方式实现
- 动态字节码增强
  - 没有接口也可以实现
  - 可以为spring aop提供扩展
- java代码生成
- 自定义类加载器
  - JBoss AOP,AspectWerkz使用此种方式
- AOL扩展
  - AspectJ使用这种方式

1. 动态代理无法对其子类进行扩展
2. 动态字节码增强进行扩展

### Spring AOP的实现机制

#### 代理模式

* 静态代理问题:Pointcut 过多操作繁琐

#### 动态代理

* 解决静态代理问题
* 缺点:只能针对实现接口的实现类,为其生成代理对象
* 示例:spring Aop
  * 发现目标对象实相应Interface,采用动态代理为其生成相应代理对象
  * 未实现任何Interface,采用CGLIB字节码增强

#### 动态字节码生成

* 扩展子类,覆写父类方法
* 限制:无法对final方法进行覆写



## 相似对比









