# 总结
本周接触了一些公司的项目代码（O2O），学习了Redis内容

## 1、Mysql
学习了一下mysql 数据库的常用点：
1、索引类型如何实用，常用的几个索引类型：普通索引，唯一索引，组合索引，主键索引，全文索引等
2、事务：什么事务 如何用 什么场景用；事务用来管理 insert,update,delete 语句，事务是必须满足4个条件（ACID）：：原子性、一致性、隔离性、持久性
3、如何排查慢sql 死锁问题；
①、show OPEN TABLES where In_use > 0;查询是否存在死锁；
②、查询死锁Itrx_mysql_thread_id  SELECT * FROM information_schema.INNODB_TRX; 
③、 kill Itrx_mysql_thread_id；解除死锁。

## 2、Redis
Redis支持五种数据类型：string（字符串），hash（哈希），list（列表），set（集合）及zset(sorted set：有序集合)。
每种数据类型都会对应一些命令，因为Redis跟map都是使用key-value这种键值对的方式进行存储数据，
Redis键命令用于管理redis的键。Redis的高级应用还没学完。

## 3、阅读公司的项目代码
本周阅读了O2O的项目的部分代码，读了facade层接口及其实现类，service层接口，model层及Controller层等代码

## 4、canal
canal基于数据库增量日志解析，提供增量数据订阅和消费，目前主要支持了MySQL；
canal工作原理实现流程：
①、canal模拟mysql slave的交互协议，伪装自己为mysql slave，向mysql master发送dump协议
②、mysql master收到dump请求，开始推送binary log给slave(也就是canal)
③、canal解析binary log对象(原始为byte流)。
