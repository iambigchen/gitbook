#### options（http1.1才支持）

​	用来查询请求URI指定资源支持的方法

​	请求： 

```js
OPTIONS * HTTP/1.1
Host: www.xxxx.com
```

​	响应：

```js
HTTP/1.1 200 ok
Allow: GET,POST
```

​	cors "预检"请求用的请求方法是`OPTIONS`，表示这个请求是用来询问的。头信息里面，关键字段是`Origin`，表示请求来自哪个源。



#### 持久连接（http1.1标准化）

特点：只要任意一端没有明确提出断开连接，则保持tcp连接状态



#### 管线化

以前发送请求后等待并接收到响应才能发送下一个请求。管线化技术出现后，不用等待响应也可以直接发送下一个请求



#### cookie

Cookie会根据服务器端发送的响应报文内的一个叫做set-cookie的首部字段信息通知客户端保存cookie。当下次客户端再往该服务器发送请求时，客户端会自动在请求报文中加入cookie值后发送出去。

服务器端发送客户端发送过来的cookie后，会去检查究竟是从哪一个客户端发来的连接请求，然后对比服务器上的记录。最后得到之前的状态信息



#### http报文

请求报文，响应报文



报文首部 （请求行， 各种首部字段） （状态行，各种首部字段）

 +

空行（CR+LF）

+

报文主体（不一定有）



请求行： 请求方法，请求uri，和http版本

状态行： 状态码，原因短语，http版本

首部字段：请求和响应的各种条件和属性的各类首部（通用首部，请求首部，响应首部，实体首部）

其他：cookie



#### 代理

代理服务器转发请求时，需要加via首部字段标记经过的主机信息

使用代理服务器理由：利用缓存技术减少网络带宽流量，组织内部针对特定网站的访问控制，以获取访问日志为主要目的

分类： 缓存代理，透明代理（不对报文做任何加工的代理称透明代理）



#### 网关

网关能使通信线路上的服务提供非http协议服务。能提高通信安全性。



#### 隧道

按要求建立一条与其他服务器的通信线路，隧道本身不会去解析http请求


