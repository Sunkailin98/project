# 总结
本周接触了一下公司的项目

## 1、自定义枚举-mybatis的字段映射
mybatis中内置了两个枚举转换器，分别是：EnumTypeHandler和EnumOrdinalTypeHandler；  
其中EnumTypeHandler是mybatis默认的转换器，该转换器将枚举实例转换成实例名称的字符串，可以理解为：Xxxx.OPEN转换为OPEN；  
EnumOrdinalTypeHandler是将枚举实例转换为实例Ordinal属性作为取值，可以理解为：Xxxx.OPEN转换为0，Xxxx.CLOSE转换为1，  
使用它的方式是要在mybatis配置文件中进行定义，配置handler和javaType（ps:进行优化后，我们可以通过干预SqlSessionFactory的创建，将转换器指定为默认的，从而可以使我们不用再写Mybatis的配置文件）

## 2、自定义类型转换器
BaseTypeHAndler<T>一共需要实现4个方法：  
####①、void setNonNullParameter(PreparedStatement ps,int i,Tparameter,JdbcTypejdbcType)  
用于定义设置参数时，该如何把java类型的参数转换为对应的数据库类型
####②、T getNullableResult(ResultSet rs,String columnName)  
用于定义通过字段名称获取字段数据时，如何把数据库类型转换为对应的java类型  
####③、T getNullableResult(ResultSet rs,int columnIndex)  
用于定义通过字段索引获取字段数据时，如何把数据库类型转换为对应的java类型  
####④、T getNullableResult(CallableStatement cs,int columnIndex)  
用于调用存储过程后，如何把数据库类型转换为对应的java类型
  
## 3、Json
JSON有两种表示结构，对象和数组。  
①、对象结构以”{”大括号开始，以”}”大括号结束。中间部分由0或多个以”，”分隔的”key(关键字)/value(值)”对构成，关键字和值之间以”：”分隔；  
（其中关键字是字符串，而值可以是字符串，数值，true,false,null,对象或数组）  
②、数组结构以”[”开始，以”]”结束。中间由0或多个以”，”分隔的值列表组成；  
（其实数组里面的内容也是键值对，只不过较对象结构不同的是，可以理解为多个对象结构组合成数组结构）

## 4、参与公司的项目
参与了国际化翻译这个模块的部分内容；  
利用canal来监听binlog信息，若数据库中的表里面的信息发生修改或者更新，会在控制台输出before（更改信息前的数据库信息）和after（更改信息后的数据库信息）  
