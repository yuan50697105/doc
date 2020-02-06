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

6. 应用实战

   

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
            2. Spring Cloud Data Flow ETL工具
         4. Spring 生态圈
            1. Spring Data
            2. Spring Security
            3. Spring Cache
            4. Spring Session
            5. Spring Task
            6. Spring AMQP
      2. Mybatis
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
3. Android
   1. Java 和 Kotlin
4. 其他扩展
   1. Groovy与Grails（全栈开发框架）
   2. Scala与Play（全栈开发框架）
   3. Helidon（Micro Profile）
   4. Micronaut
   5. quarkus

## 4.语言

1. Kotlin
2. Scala
3. Groovy

## 5.构建与依赖管理工具

1. Maven
   1. Maven使用
      1. 创建项目
      2. 生命周期
      3. archtype
      4. 插件
      5. 多模块
      6. 预配置
   2. MVNW
      1. 解决问题
      2. 生成
      3. 使用
2. Gradle
   1. Gradle使用
      1. 创建项目
      2. 生命周期
      3. basic project
      4. 插件
      5. 多模块
   2. Gradlew
      1. 解决问题
      2. 生成
      3. 使用

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

# Linux学习

1. 了解发行版
2. 基础命令
3. 安装软件
4. 账户与授权
5. 打包镜像，不过现在主要是容器化了

# 持续集成

## 1.自动构建 Jenkins

## 2.容器化 docker

## 3.容器编排 Kubernetes /Meaos

# JS与前端学习

## 1.HTML

## 2.CSS

## 3.JS与TS

## 4.Node与Deno（Deno 目前没有发行，可能是下一代Node）

### 	1.Commons JS

### 	2.ES6 ES7 ES8

1. 这个是个标准定义，但是并不是完全实现，语法很灵活，受不了

### 	3.Express Koa

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

### 	1.Flask

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

