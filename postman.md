# 1. Postman设置环境变量

1.点击postman右侧的小眼睛，在Environment 处点击Add

2.设置环境名，变量名(注意:变量名都一致，建议为url),默认变量值，当前变量值。可以设置多个进行环境切换

3.使用 {{Variables}} 的形式引用

# 2. Postman 如何处理上一个接口返回值作为下一个接口入参

比如，每次调用一个接口之前都需要获取一次token。



现在token的接口中的test中如下书写:

``` javascript
var jsonData = JSON.parse(responseBody);
pm.globals.set("token", jsonData.data);
```

这里把"token"设置到了全局变量。

就可以进行全局引用了。



我们只需要在调用接口之前先调用一次token接口，不在需要手动复制值(token)到要调用的接口。
