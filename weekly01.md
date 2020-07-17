# 总结
本周运用了IDEA进行了SSM框架的整合，学习了SSM框架中的注解还有spring中的注解，学习了maven的开发运用以及pom.xml、applicationContext.yml等文件的基础配置

## 1、Spring回炉
首先是系统的回炉了spring的IOC/DI和AOP等技术，spring的IoC容器是spring的核心，spring AOP是spring框架的重要组成部分，IOC我的理解是原由程序员手动通过new实例化对象的事情转交给了Spring容器负责，
它最大的作用是“解耦”，解的是程序员与对象管理之间的耦合；AOP在原有的正常程序执行流程中，添加了一个横切面，在不改变原来的程序代码及程序功能的前提下，释放了部分逻辑，让职责更加明确

## 2、注解
使用注解可以让开发变得简易许多，会使代码的量减少，不会看着那么臃肿。
使用@interface可以进行自定义注解，并且元注解（可以加在注解上的注解）共有五个@Retention、@Documented、@Target、@inherited、@Repeatable
ssm框架中的注解有很多种类，用于创建对象的注解（Component），用于改变作用范围的注解（Scope），用于注入数据的注解（@Autowired）等
还有SpringBoot中的一些注解，这些注解有的在项目工程中会用的很频繁，可以在练习等方式进行加以理解及运用

## 3、Spring Boot
在此期间着手学习了***Spring Boot***，初步掌握了它的自动配置和起步依赖，他的起步依赖可以理解为将具备某种功能的坐标打包到一起，并提供一些默认的功能，使用springBoot需要在pom.xml文件中引入依赖
***spring-boot-starter-parent***和启动器***spring-boot-starter-web***，并在applicationContext.yml文件中进行配置，格式key：value，value前面要有一个空格，编写启动程序：application.class

## 4、消息队列（MQ)
消息队列的主要作用是解耦，***消峰***和异步，了解了MQ中的基本术语，消息生产者，消息消费者，中间经纪人等，在使用rockwtMq前要先启动namesrv和broker，查看官网的文档，进行了解他的一些消息传递模型并进行代码的联系
（消息队列这一块内容掌握的不是特别熟悉，计划准备配合一些视频讲解进行补充学习）

## 5、 Redis
看了一点Redis的内容，类似于集合中的map，都是用key-value这种键值对的方式进行存储数据，周末找时间再系统的学习一下Redis

## 6、练习
本周完成了一个简易的图书管理系统，利用spring+springBoot+mybatis等框架技术实现了基本的增删改查功能，并实现了通过id可以查询该用户是否已经存在及分页显示等简易功能
 
