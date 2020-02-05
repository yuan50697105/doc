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

   1. if
   2. if (){}else{}
   3. if (){}else if{}

2. switch

   case

   default

   break

   > switch注意事项
   >
   > 1. 自从JDK 1.7 开始 case可以使用字符串，但是不能使用封装类，请使用里面的API转换成关键字
   > 2. JDK 13 新增模式匹配功能，这个功能在很多语言中存在了，加上这个以后，可以很大程度上扩展语法

### 1.3 循环

1. for(   ;    ;   )
2. for(Object object : Iterable/Array)
3. while(boolean)
4. do{} while(boolean)

### 1.4 方法（函数）

1. void 无返回值
2. 返回值为基础数据类型 封装类
3. 返回值为封装类数组
4. 返回值为封装集合
5. 返回自定义类或者接口
6. 返回自定义类或者接口数组或集合

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

   1. 字节流
   2. 字符流
   3. 随机流
   4. NIO与BIO（NIO非阻塞IO，BIO阻塞IO，我们常用的是阻塞IO，所以一般实际使用的时候，非常占用资源）

4. 线程

   1. Thread
   2. Runnable
   3. Callable
   4. Future

5. socket（主要是TCP和UDP内容，还有基础工具类使用）

6. GUI（基本不会学了）

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

1. Spring
   1. Spring MVC
   2. Spring Boot
   3. Spring Cloud
2. Hadoop
3. Spark
4. Android
5. 其他扩展

## 4.语言

1. Kotlin
2. Scala
3. Groovy

## 5.构建与依赖管理工具

1. Maven
2. Gradle

# Linux学习

1. 了解发行版
2. 基础命令
3. 安装软件
4. 账户与授权
5. 打包镜像，不过现在主要是容器化了

# 持续集成

自动构建 Jenkins

容器化 docker

容器编排 Kubernetes /Meaos

# JS与前端学习

1. HTML
2. CSS
3. JS与TS
4. Node与Deno
5. WASM

# Python学习

# Golang学习

# Rust

# Ruby

# IDE工具

## 1.IDEA

1. 配置
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

