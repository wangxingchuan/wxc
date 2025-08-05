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
