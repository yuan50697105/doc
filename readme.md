# Java学习

## 1.基础内容

### 1.1 数据类型

| 中文名称   | 关键字  | 封装类    | 注意事项             |
| ---------- | ------- | --------- | -------------------- |
| 整型       | int     | Integer   |                      |
| 长整型     | long    | Long      | java中最大的整数     |
| 短整型     | short   | Short     |                      |
| 字节       | byte    | Byte      | 这个是最小的整型数据 |
| 单精度浮点 | float   | Float     |                      |
| 双精度浮点 | double  | Double    | java中最大的数字     |
| 布尔       | boolean | Boalean   | 逻辑判断             |
| 字符       | char    | Charactor | 不是String字符串     |

> 注意事项：
>
> 1. java中没有无符号数定义，所以java中最大值小2倍
> 2. String（字符串不是基础数据类型）
> 3. java处理数字型数据是按照int->long->double顺序处理，即使使用short和byte，java也是按照int处理，float默认按照double处理，float不能直接使用
> 4. 自从JDK1.5 开始关键字和封装类通用，不过尽量不要用关键字和封装类直接==或者equals

### 1.2 逻辑处理

1. if

   1. 介绍使用boolean 结果，处理分支，注意一个if只有一个分支，if else只有两个分支
   2. if(){}
   3. if (){}else{}
   4. if (){}else if{}

2. switch

   1. 一个多分支处理，不过建议使用枚举或者常量
   2. case 条件，不过只能是固定条件
   3. default 默认条件 ，只有case不能匹配到时才会执行
   4. break 如果没有return 用于退出switch

   > switch注意事项
   >
   > 1. 自从JDK 1.7 开始 case可以使用字符串，但是不能使用封装类，请使用里面的API转换成关键字
   > 2. JDK 13 新增模式匹配功能，这个功能在很多语言中存在了，加上这个以后，可以很大程度上扩展语法

### 1.3 循环	

1. 介绍，用于重复执行，一段代码
2. for(   ;    ;   )
3. foreach for(Object object : Iterable/Array)
   1. Iterable是可迭代的统配，集合类中的List和Set都是可迭代
   2. Array数组
   3. foreach 不能再往遍历的数据中写入数据，也就是说foreach是只读的
4. while(boolean)
5. do{} while(boolean)
6. break 跳出循环
7. continue 跳过一次循环

### 1.4 方法（函数）

1. void 无返回值
   1. void无参数
   2. void 有参数
      1. 一个参数
      2. 多个固定参数
      3. 不定项参数
      4. 混合使用，不定项最多一个且在最后
2. 有返回值
   1. 返回值为基础数据类型和封装类
   2. 返回值为封装类数组
   3. 返回值为封装集合
   4. 返回自定义类或者接口
   5. 返回自定义类或者接口数组或集合
   6. 参数处理
      1. 一个参数
      2. 多个固定参数
      3. 不定项参数
      4. 混合使用，不定项最多一个且在最后

### 1.5 类与接口

1. 类的定义，用来描述一种事物，他的实例化被称为对象，会分配堆内存

   1. 基础原则，高内聚，低耦合，单一责任
2. 存在形式
   1. class 基础类

   2. final class 终结类 不能继承

   3. abstract class 抽象类，不能直接实例化，专门用继承扩展

   4. inner class 内部类 

      1. 类中类 
3. 访问控制

   1. public 只要声明就能在任何外部类中访问
   2. protected 必须是继承的子类可以内部访问
   3. private 只能在类内部使用
   4. default 只能在同一个包下面使用，这个是默认就是上面三个都不存在时，jdk1.8 在接口上有特殊定义
4. 接口

   1. 一种特殊的存在，使用上与抽象类相似，在JDK1.8以前，可以说只有声明，但是1.8以后增加默认实现default功能，简单来说就像抽象类了
5. 反射
6. 自省
7. 应用实战


### 1.6 数组

## 2.基础内容与常用工具集

### 2.1 基础内容

1. 集合类

   1. List
   2. Set
   3. Map
   4. Iterable
   5. Collection

2. String三剑客

   1. StringBuilder
   2. StringBuffer
   3. StringJoiner JDK8 新增

3. IO类

   1. IO是两个部分，I-> Input，O->Output，
   2. 使用注意 In和Out两个是相对概念，如果是程序往外输出就是Out，接收方就是In
   3. 字节流 InputStream和OutputStream
   4. 字符流 Reader和Writer
   5. 随机流 
   6. NIO与BIO（NIO非阻塞IO，BIO阻塞IO，我们常用的是阻塞IO，所以一般实际使用的时候，非常占用资源）（NIO部分我自己还没有学习）

4. 线程

   1. Thread
   2. Runnable
   3. Callable
   4. Future
   5. JUC 并发工具

5. socket（主要是TCP和UDP内容，还有基础工具类使用）

6. GUI（已过时，基本不会学了）

7. JDBC

   1. 用于关系型数据库连接统一接口
   2. 适用数据库 MySQL，Oracle，SQL server ，Postgres，MariaDB

8. Servlet

   1. Java web基础 最新版本4.1
   2. 域对象（九个，目前常用五个个）
      1. request 请求
      2. response 响应
      3. session 回话，用于保存用户信息
      4. application 全局信息
      5. out 输出，一般是用在JSP或者模板上，现在基本上只是用来输出JSON或者XML
      6. filter 过滤器，又称连接器
      7. listener 监听器，用于全局动态配置

9. JDK8 特性 

   1. Stream API

   2. Function 从JDK8开始可以直接把函数作为参数使用了，总计六个扩展

   3. Optional 可选放空判断

      > 上面三个是组合使用的

10. JDK9 特性（no LTS，非长期支持下同）

    1. 模块化 没什么卵用
    2. JShell 即时编程
    3. 增加HTTP 客户端
    4. 增加RX编程API

11. JDK10 特性（no LTS）

    增加 var自动推断关键字，这个关键字必须实例化，如果是低于这个版本可以用lombok的扩展

12. JDK11 特性（LTS）

    增加ZGC（实验性）

    扩展Stream

13. JDK12 特性（no LTS）

    switch扩展（实验性）

14. JDK13 特性（no LTS）

    switch 模式匹配

### 2.2 常用工具集（大厂扩展）

1. Apache Commons 主要是一些方便的工具集
2. Jadd 工具及扩展
3. Google Guava 主要是集合，缓存扩展，功能大量使用建造者模式
4. Hutool国内集成不错的

## 3.Java APP

1. Java Web
   1. Spring
      1. Spring
         1. Spring MVC
         2. Spring Boot
            1. Spring MVC
            2. Spring Webflux
         3. Spring Cloud
            1. 微服务应用
            2. Spring Cloud Data Flow —— ETL工具
            3. Spring Cloud Function —— Serverless 
         4. Spring 生态圈
            1. Spring Data
               1. Spring Data JDBC
               2. Spring  Data JPA
            2. Spring Security
            3. Spring Cache
            4. Spring Session
            5. Spring Task
            6. Spring AMQP
            7. Spring Kafka
         5. 技术栈
            1. Spring Servlet
            2. Spring Reactor
      2. Mybatis
         1. 基本使用
         2. 功能扩展（拦截器，插件机制）
         3. 常用扩展
            1. Pagehelper
            2. SQLHelper
            3. TkMapper
            4. Mybatis Plus
      3. Hibernate
2. 大数据
   1. Hadoop
      1. HDFS
      2. Yarn
      3. MapReduce
      4. HBASE
      5. Hive
   2. Spark
      1. Scala API、Python API、Java API
      2. Spark RDD
      3. Spark SQL
      4. Spark Straming
   3. Flink
      1. Java API 、Scala API
      2. Flink Stream
      3. Flink SQL
   4. Solr与ES
3. Android
   1. Java 和 Kotlin
4. 其他扩展
   1. Groovy与Grails（全栈开发框架）
   2. Scala与Play（全栈开发框架）
   3. Helidon（Micro Profile 基于Java EE定制的微服务与云原生开发组件）
   4. Micronaut（Grails作者做的微服务框架）
   5. quarkus（基于Kubernetes 的Java微服务框架，由Kubernetes的运维组织制作）

## 4.语言

1. 关于Java是分成Java语言和JVM两个部分只要是能编译成JVM使用的字节码就能使用使用JVM环境
2. Kotlin
   1. 由目前最流行的Java IDE工具IDEA的开发商Jetbrain开发的语言，推出之后得到谷歌深度支持成为安卓第一开发语言，而且Spring官方也深度支持，另外很多其他框架也在深度支持，所以现在做java的不单单是学习Java一种语言了，必要时候也得学习下Kotlin，他和Java是100%兼容的，所以基本上能够无缝使用java的依赖库，可以使用Maven和Gradle构建环境，不过比较建议使用Gradle构建
   2. 相比Java 最大的进步主要是协程结束，还有一些灵活定义
   3. Kotlin生态
      1. Kotlin JVM
         1. 也就是在JVM上运行
      2. Kotlin JS
         1. 使用Kotlin JVM语法配置JS和TS的API实现，可以在浏览器和Node上运行
      3. Kotlin Native（试验中）
         1. 主要是面向无虚拟机环境使用，比如IOS
      4. Kotlin Data Science（新增）
         1. 这个是新增功能，开始挑战Python
      5. 总结，不服就干，生死看淡
3. Scala
   1. 一个高扩展JVM语言，其实还有JS版本，不过主要是使用JVM版本，这个语言灵活度很高，不过有些地方概念深，不好入门，入门的话灵活度很强，就是概念多，灵活度高，所以入门难，主要是用在Spark分布式计算上
   2. 优势是高扩展
   3. 国内除了使用在Spark上，其他很少使用
4. Groovy
   1. JVM脚本语言，作者也是看着Java表达繁琐，所以想像JS那样简单直接，所以做了Groovy，不过现在Groovy这个语言用的很少了
   2. 加入函数式语法和模板语法
   3. 当前现状，除了Gradle 和Grails 其他的平台很少使用了

## 5.构建与依赖管理工具

1. Maven
   1. Maven使用
      1. 创建项目
         1. basic
            1. 基础版本
         2. archtype
            1. 模板版本
            2. 常用
               1. WEB
      2. 生命周期
         1. 三个
            1. 清理生命周期
               1. pre-clean 预清理
               2. clean 清理
               3. post-clean 清理后
            2. 默认生命周期
               1. process-resources 复制并处理资源文件，至目标目录，准备打包。
               2. compile 编译项目的源代码。
               3. process-test-resources 复制并处理资源文件，至目标测试目录
               4. test-compile 编译测试源代码
               5. test 使用合适的单元测试框架运行测试。这些测试代码不会被打包或部署。
               6. package 接受编译好的代码，打包成可发布的格式 
               7. install 将包安装至本地仓库，以让其它项目依赖
               8. deploy 将最终的包复制到远程的仓库，以让其它开发人员与项目共享。
            3. 站点生命周期
               1. pre-site（预站点）：执行一些需要在生成站点文档之前的工作。
               2. site（站点）： 生成项目的站点文档。
               3. post-site（后站点）：执行一些需要在生成站点文档之后完成的工作，并且为部署做准备。
               4. site-deploy（站点部署）：将生成的站点文档部署到特定的服务器上
         2. 插件
            1. 有些通用操作有可以使用专用插件，这个也是配合生命周期来的，maven自己也提供了很多默认的插件
            2. 默认插件
               1. clean
               2. compile 编译插件，提供基本的编译功能，比如java版本
               3. package 打包
               4. jar 打包成jar包，jar分成lib和exe两种类型，exe的要配置mainClass
               5. war javaweb特制的jar，现在基本上没有用的了
               6. shade 定制打包
               7. denpendency 依赖管理
               8. install 将package打包以后的jar放入本地maven仓库
               9. deploy 将本地仓库的jar推送到远程仓库，一般用于企业仓库私服
            3. 常用插件
               1. versions 用于模块的版本控制，依赖升级等
         3. 多模块
            1. maven是支持多模块module的，而且可以多级嵌套
         4. 预配置
            1. profile
         5. 构建语法 XML  POM
      3. 使用 mvn
   2. MVNW
      1. 解决问题 mvnw是为了解决本地没有maven或者不满足版本要求使用的，使用时会自动下载对应的maven版本进行上面的生命周期操作和插件操作
      2. 生成 maven官方未提供生成，不过也基本上不用担心这个我用了2年基本没发现不兼容，可能是现在maven整体定型和稳定了
      3. 使用 mvnw 加上原来mvn命令即可
   
2. Gradle
   1. Gradle使用
      1. 创建项目
      
         1. basic
         2. java
         3. groovy
         4. kotlin 
         5. cpp
         6. swift
      
      2. 生命周期
      
         1. Initialization
      
         2. Configuration
      
         3. Execution
      
      3. basic project
      
      4. 插件
      
      5. 多模块
      
      6. 构建语法
      
         1. Groovy DSL
         2. Kotlin DSL
   2. Gradlew
      1. 解决问题 同 mvnw，gradle本身可以生成，gradle每个大版本都有API变化，所以为了防止不兼容所以经常使用这个
      2. 生成 gradle wrapper
      3. 使用 gradlew 加上gradle基本命令
   
3. Maven和Gradle对比

   1. Maven 约束规范严格，插件多，省资源，因为使用XML约定，所以语法上比较啰嗦
   2. Gradle 语法灵活，构建快，但是冷启动慢，大项目因为要常驻一个java后台，所以比较费内存，小内存慎用，使用Groovy或者Kotlin的定制DSL语法，使用灵活高效，可以使用必要的编程特点实现

## 6.框架与技术栈内容

1. Spring
   
   1. Spring
      1. 简介：一个用于快捷依赖注入的框架，核心内容是IOC（控制反转）和AOP（面向切面）
      2. IOC：一个注入模式，核心是工厂模式和单例模式，这个有多种模式，如果不和MVC一起用可以有单例和原型模式，加入Web后可以用Session和Request
      3. APO：核心是装饰器模式，用于整个方法执行过程的包装监控，经典使用就是MVC和事务处理
      4. Reactor：Spring 5.0 新增技术栈，以观察者模式实现异步高吞吐量技术，不是直接提升性能，而且将并发能力提升
   2. Spring WEB
      1. Spring MVC
         1. 简介：Spring中 Web模块扩展，可以直接实现HTTP访问，使用Servlet标准实现
      2. Spring WebFlux
         1. 简介：Spring中 Web模块扩展，可以直接实现HTTP访问，全新Reactor技术栈实现
      3. 其他扩展
         1. Struts
   3. Spring JDBC与Spring ORM
      1. 简介：Spring提供的基本关系数据库访问功能
   4. Spring Data
      1. 简介：Spring 在JDBC和ORM基础上增加的统一访问功能
   5. Spring Cache与Spring Session
      1. Spring Cache 
         1. 简介：缓存抽象，用于数据缓存
      2. Spring Session
         1. 简介：用于Session管理控制
   
   1. Spring Security
      1. 简介：Spring自己的权限框架，细粒度很高，可以与Spring Session无缝组合
   2. Spring Boot
      1. 简介：以约定大于配置方式实现自动化配置的方案，目前主要方案，提供可执行jar方式部署
   3. Spring Cloud
      1. 简介：在Spring Boot基础上扩展出来的微服务方案
   4. Spring On K8S
   
2. Hibernate

   1. 简介： 一个持久框架，提供常用数据库的快捷操作，提供分页列表操作，但是没有分页模型
   2. JPA ：JPA是个Java 的标准，用于持久层实现，他的第一实现就是Hibernate，但是Hibernate也增加了自己的东西
   3. Spring Data Jpa ：Spring Data 组件之一，在Jpa上封装

3. Mybatis

   1. 简介 一个持久层框架
   2. Mybatis Mapper：Mybatis扩展 ，一个Mybatis单表操作框架，使用类似Mybatis 逆向工程的Example风格编程
   3. Mybatis Plus： Mybatis 扩展，这个扩展做的应该算是非常好了，主要是集成了分页
   4. Mybatis Enhance：Mybatis扩展，作者仿造Spring Data Jpa和QueryDSL 风格制作，需要使用生成器
   5. FastMybatis： Mybatis 扩展，单表操作方便，提供分页功能，只限制为单表
   6. PageHelper： Mybatis 分页助手，直接能在mybatis查询时实现分页，提供分页模型
   7. SqlHelper：Mybatis 分页助手，可以转换为PageHelper 风格，提供Mybatis Plus集成
   8. Pageable：Mybatis 分页助手 
   9. 特殊用法 插件机制，可以实现自动添加功能
   10. 类型处理器，比如JSON，Array的处理

4. JOOQ

   1. 简介：以Fluent API 风格进行数据库操作，跟使用SQL基本相同，提供分页列表，但是没有分页模型，只有Mysql和Postgres时免费使用，Spring Boot 提供自动配置

5. Query DSL

   1. 简介：一个通用安全查询框架，有JDBC，JPA等多个版本，其中Spring Data Jpa 提供扩展接口

6. 数据库中间件

   1. Apahce Sharding
      1. 简介 一个数据分片框架
      2. 使用 根据官方说明使用即可
      3. bug 主键策略一直是个问题
   2. MyCat

7. Redis 

8. MongoDB

9. ElaticSearch

10. CouchBase

11. FluxDB

12. Hadoop

    1. 简介：通用计算分析，储存框架
    2. 计算
       1. MapReduce， 离线计算，模型已经过时，同时性能低
       2. Hive，目前Hive已经基本放弃MapReduce了
    3. 储存
       1. HDFS， 分布式文件系统，可以多副本，一般用于大数据缓存，一次写入，多次读取
       2. HBASE， 在HDFS基础上建立的高性能列族数据库
       3. Hive， Hive可以说是计算也是一个结构化数据储存
    4. ETL 数据抽取，转换、加载
       1. Sqoop 分成两个版本，两个版本几乎完全不同，用于多个数据源直接ETL
       2. Flume 日志收集ETL

13. Spark

14. Flink

# SQL学习

1.介绍

​	结构化查询语言，广泛应用于数据库软件中，用于查询统计增删改

2.标准定义

​	SQL的标准不是一直不变，现在新版本的标准中增加了JSON，Array，开窗函数等定义，但是并不是所有库都实现了

3.学习

1. 整体分成四个部分
2. DCL 权限控制 这个很多是使用工具来做，不过Oracle要使用SQL配置，不同数据库完全不同
3. DDL 结构定义 一般用工具做，还有关系生成公具做，不同数据库，总体一样，数据类型不一样
4. DQL 查询统计 最常用的 select，不同数据库存在自己特异的查询统计函数
5. DML 数据操作 也就是增删改

4.常见数据库与相关

1. 数据库：MySQL（标准SQL），Oracle（PLSQL+标准SQL）、SQL Server（TSQL+标准SQL）、PostgresSQL（PSPLSQL+标准SQL）、MariaDB（标准SQL）
2. 仓库类：Hive
3. 类SQL库：Cassandra

5.误区

1. 拥有SQL或者类SQL解析执行能力的数据库，都有自己特有的部分和公共基础的部分，基础实现都不同，部署方式也有差别

6.具体数据库

1. MySQL
   1. 最流行数据库
   2. 功能实现基本按照标准来
2. Oracle
   1. 大型数据库代表，在高性能服务器上能够成分发挥性能，不过授权非常规
   2. 功能强大
3. SQL Server
   1. 第三大数据库，由微软开发，在分布式上有点优势，应用与企业项目和工业项目多
4. Postgres
   1. 被称为最先进数据库，因为他是实现SQL标准最完善的，同时他是完全开源的，被称为开源的Oracle

# Linux学习

1. 了解发行版
   1. RH 红帽
   2. Federa  红帽弄得专门用于云原生的发行版
   3. CentOS 红帽源码重编版本
   4. Debian 
   5. Ubuntu 最流行的桌面Linux
   6. 区别红帽和Debian是两个不同的大发行版，因为内部实现不相同
2. 基础命令
   1. mv 移动文件或者重命名问价
      1. mv 源文件或者目录 新文件名或者目录
   2. cp 拷贝文件
      1. cp 源文件或者目录 新文件或者目录
   3. rm 删除
      1. -r 删除目录
      2. -f 强制删除
      3. 常用 rm -rf 组合使用，但是切记不要早root权限下使用 rm -rf /*
   4. ln 软链接（与windows的快捷方式一样就是个指针）
3. 安装软件
   1. yum (红帽系，cent os,federa,rhel)
   2. apt（debain系，debain，Ubuntu）
4. 账户与授权
   1. group 用户组
      1. groupadd
      2. groupdel
      3. groupmod
   2. user 添加账户
      1. useradd
      2. userdel
      3. usermod
   3. chmod 授权
      1. 三组RWX 
         1. 用户 u
         2. 组 g
         3. 同组 o
      2. 使用
         1. chmod -R 777 目录或者文件
   4. chown 授权所属用户
   5. chgrp 授权所属组
5. 压缩与解压缩
   1. tar
      1. 参数
         1. -c 创建压缩包
         2. -x 解压缩  
         3. -z tar.gz
         4. -j tar.bz
         5. -f 文件名
         6. -O 输出目录
   2. zip
      1. 安装unzip
   3. rar
6. 打包镜像，不过现在主要是容器化了
   1. 

# 持续集成

## 1.自动构建 Jenkins

## 2.容器化 docker

## 3.容器编排 Kubernetes

## 4.Rancher

## 5.Serverless 无服务架构 Knative 、Istio、Kubernetes、Linkerd

# 部署结构

1. 集中式
   1. 全集中
   2. 垂直分离
   3. 集群负载均衡
   4. 垂直分离+集群负载均衡
2. 分布式
   1. SOA
   2. MSA
   3. FSA（Serverless 核心点）

# JS与前端学习

## 1.HTML

## 2.CSS

## 3.JS与TS

1. JS Javascript
2. TS TypeScript

## 4.Node与Deno（Deno 目前没有发行，可能是下一代Node）

1. Node 基于Chrome V8 引擎制作的服务端JS运行环境

### 	1.Commons JS

### 	2.ES6 ES7 ES8

1. 这个是个标准定义，但是并不是完全实现，语法很灵活，受不了

### 	3.Express Koa

1. Express Web开发框架
2. Koa Web开发框架，Express 团队新作

### 	4.Vue

### 	5.React

### 	6.Angular

## 5.WASM（第四标准，用于二进制传输）

# Dart与Flutter

## 1.介绍

​	Flutter由谷歌开发的通用应用层框架，一套语法，多端开发，使用Dart语言

# IOS与Swift

## 1.介绍

​	IOS是苹果开发的手机iPhone的操作系统，目前iPad使用的操作系统改名为iPad OS，电脑Mac系列成为Mac OS，Swift是由苹果自己开发的用于自己平台的开发语言，目前已经开源，Windows平台非官方支持

# Python学习

## 1.数据类型

## 2.基础变量

## 3.方法

## 4.面向对象

## 5.基础库

## 6.web

### 		1.Flask

### 7.爬虫

### 8.人工智能

1. 关于人工智能为什么使用Python的误解，这个主要是Python在发展过程长期被用于数据科学计算，加上语法简单，产生了相关库特别多，但是Python几乎所有与人工智能相关的组件都是有更高性能的语言开发，加上Python的壳，所以Python常常被说成胶水语言

### 9.数据科学

1. 一般用于做报表用

### 10.自动运维脚本

# Golang学习

### 1.介绍

​	由谷歌开发，开发人员为C语言作者，所以性能很高，是个用基础软件开发的语言，特别是多核心并发并行上有特殊之处，不过针对对象化、泛型、依赖管理是个劣势，主要是用于容器软件（Docker，Kubernetes )，区块链

# Rust学习

## 1.学习理由

新语言，微软将用它重构基础组件，这个我看了评论确实不错，不过微软重构是自己在Rust 的基础上改进，就像微软喜欢Java，自己弄了个.Net，这个新语言的维护者就是C#的作者

# Ruby学习

## 1.学习理由

​	这个语言和python基本一个性质，其实主要是Vue那边有个CSS框架

# dotNet学习

# IDE工具

## 1.IDEA

1. ###### 配置

   1. 忽略大小写

2. maven配置

3. gradle配置

4. 常用插件

   1. lombok
   2. allsetter
   3. mybatiscodehelperpro（付费）

5. 快捷键

   1. 

## 2.Eclipse

1. 配置
2. maven
3. gradle
4. 常用插件
5. 快捷键

