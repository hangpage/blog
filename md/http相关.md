- TCP/IP分层 
1. 应用层  为用户提供应用的接口 dns位于应用层，用来进行域名解析
2. 传输层  对接上层应用层，提供处于两台计算机之间的数据传输
3. 网络层 通过网络传输数据
4. 数据链路层 用来处理连接网络的硬件部分

- 三次握手
握手过程使用TCP标志 SYN和ACK，
发送端发送SYN给对方，
接收端接受到之后，回传SYN和ACK标志数据包表示确认信息，
最后发送端回传ACK，代表握手结束。

URI 统一资源标识符 URL统一资源定位符
协议方案：http ftp file等

1.1中 http默认为持久化链接，节省开销。 1.1之前需要设置通用首部字段connection：keep-alive表示持久化连接
管线化 并发请求

2XX 成功

- 204 no content
请求成功，但返回的响应报文不包含主体部分，一般是只需要客户端发送信息，不需要接收信息的场景。
- 206 partial content 
范围请求,响应报文只包含content-range指定范围内的内容.

3XX 重定向 表示浏览器需要执行某些特定的处理以正确处理请求
- 301 move permanently
永久性重定向, URI无法定位到资源
- 302 found
临时性重定向，表示请求的资源已经被分配到新的URI，希望用户本次使用新的URI访问
- 303 see other
表示请求的资源存在另一个URI，应使用get方法获取请求的资源。
- 304 not modified
和重定向无关，客户端发送附带条件的请求时，服务端允许请求，但未满足条件的情况下，304被返回，不包含任何响应的主体部分。
- 307 temporary redirect 
类似于302 但是不会把post变成get

> 当301 302 303响应返回时，几乎所有的浏览器都会把post变成get

4XX 客户端参数错误
- 400 bad request
请求报文存在语法错误 一般是参数错误
- 401 unauthorized
http认证失败
- 403 forbidden
访问权限问题
- 404 not found
5XX 服务端错误
- 500 Internet server error
服务器错误
- 503 service unavailable
服务器不可用 


### 代理
- 缓存代理
资源缓存在代理服务器上，减少网络带宽流量，不用从源服务器获取资源。
- 透明代理
不对请求报文做处理的代理类型称为透明代理

### 隧道 ssl加密通信


### 缓存 
代理服务器缓存与客户端浏览器缓存


### websocket 一次握手
服务器主动向客户端发送数据的能力
长连接 通信量减少

### 4中http首部字段类型
- 通用首部字段
cache-control 控制缓存的行为
connection 逐跳首部、连接的管理
date 创建报文的日期时间
pragma 报文指令

- 请求首部字段
- 响应首部字段
- 实体首部字段

### http与https的区别
