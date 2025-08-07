# spring 源码

## refresh()方法

### 1. prepareRefresh()

清除ClassPathBeanDefinitionScanner的缓存

![](file://C:\Users\wWX1334749\AppData\Roaming\marktext\images\2025-08-05-14-29-50-image.png?msec=1754375390192)

### 2.prepareBeanFactory(beanFactory)

### 3.postProcessBeanFactory(beanFactory)

### 4.invokeBeanFactoryPostProcessors(beanFactory)

会调用ConfigurationClassPostProcessor的processConfigBeanDefinitions。

调用ConfigurationClassParser.parse方法

最终会调到ComponentScanAnnotationParser.parse方法

获取basePackages，截取出现的最后的一个`.`之前的字符

![](file://C:\Users\wWX1334749\AppData\Roaming\marktext\images\2025-08-05-15-21-28-image.png?msec=1754378488829)

![](file://C:\Users\wWX1334749\AppData\Roaming\marktext\images\2025-08-05-15-20-48-image.png?msec=1754378448429)

### 5.registerBeanPostProcessors(beanFactory)

### 6. finishBeanFactoryInitialization(beanFactory)




版本发布涉及三个大类，
	1. 面向生产，服务，合作方，一线等渠道的软件发布(内部测试，聚信及EMS厂商，一线准入，第三方认证机构，用服，消费者，供应链及EMS厂商，矿鸿，测试用户，产品研发，Beta测试用户，消费者，合作方)
	2. 面向消费者的软件发布(用于政企客户，用服(Beta测试用户，消费者，保修，高维))等
面向开发者的软件发布 (测试用户，开发者)![Uploading image.png…]()

