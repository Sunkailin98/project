# 总结
本周参与了公司的项目，并在参与项目过程中补缺自己不足的短板

## 1、
本周主要进行了公司温超项目中国际化翻译这个模块，通过aop进行接口的拦截，然后再handler中进行业务逻辑的处理  
先将传入进来的数值字段进行判断，判断一下是否为空值，传入的可能是一个对象，也可能是一个集合，如果是集合则还要遍历集合，将集合中需要处理的字段拿出来后进行处理，在进行集合遍历的时候会用到lambda表达式
在处理结算页模块的时候，有的字段没有方法的调用，因此要进行map的键值对传值输入，在每次集合遍历完最后一定要set一下值，在处理字段时，一定要理清并运用好枚举类型，因为在国际化处理这块内容中，很多代码都有一块是相同的（Long bizId, String moduleName, String bizType, String languageType），所以我们可以将这块传值的代码进行抽取整合组成一个方法，共其他业务处理的时候调用，然后用postman进行接口的测试，根据花瓶的抓包进行选择合适的配置参数等，最后再dice平台进行最后的测试检验
