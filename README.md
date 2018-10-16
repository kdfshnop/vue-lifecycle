# 跨域请求的几种方式

```
1.document.domain+iframe;
2.动态创建script，因为script标签不受XmlHttpRequest同源策略的限制;
3.window.name+iframe;
4.window.postMessage;
5.cors;
6.jsonp;
7.nginx反向代理;
8.websocket;
```