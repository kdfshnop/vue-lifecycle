# get和post的区别
## get
```
1. get在浏览器回退时是无害的，而post会再次提交请求;
2.get产生的url地址可以被bookmark，而post不可以;
3.get请求只能进行进行url编码，而post支持多种编码方式;
4.get请求参数会被完整保留在浏览器历史记录里，而post中的参数不会被保留;
5.get请求会背了浏览器主动cache，而post不会，除非手动设置;
6.get请求在url中传送的参数是有长度限制的，而post没有限制；
7.对参数的数据类型，get只接受ASCII字符，而post没有限制;
8.get比post更不安全，因为参数直接暴露在url上，所以不能用来传递敏感信息;
9.get参数通过url传递，post放在request body中;
10.get产生一个TCP数据报;post产生两个TCP数据包;get从浏览器到服务器相应只需一步，而post需要两步，因此get比post请求时间短;

```