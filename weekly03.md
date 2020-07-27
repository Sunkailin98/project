# 总结
本周接触了一些公司的项目代码

## 1、自定义枚举-mybatis的字段映射
mybatis中内置了两个枚举转换器，分别是：EnumTypeHandler和EnumOrdinalTypeHandler，
其中EnumTypeHandler是mybatis默认的转换器，该转换器将枚举实例转换成实例名称的字符串，可以理解为：Xxxx.OPEN转换为OPEN；
EnumOrdinalTypeHandler是将枚举实例转换为实例Ordinal属性作为取值，可以理解为：Xxxx.OPEN转换为0，Xxxx.CLOSE转换为1，
使用它的方式是要在mybatis配置文件中进行定义，配置handler和javaType；

## 2、自定义类型转换器
BaseTypeHAndler<T>一共需要实现4个方法：
####①、void setNonNullParameter(PreparedStatement ps,int i,T parameter,JdbcType jdbcType)
用于定义设置参数时

## 3、Redis
Redis支持五种数据类型：string（字符串），hash（哈希），list（列表），set（集合）及zset(sorted set：有序集合)。
每种数据类型都会对应一些命令，因为Redis跟map都是使用key-value这种键值对的方式进行存储数据，
Redis键命令用于管理redis的键。Redis的高级应用还没学完。

## 4、阅读公司的项目代码
本周阅读了misc程序的代码，读了facade层接口及其实现类，service层接口，model层及Controller层等代码，查看理解misc-web层以及他的启动层（misc-web-starter）
