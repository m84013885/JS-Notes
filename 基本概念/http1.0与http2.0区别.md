### http升级优化最显著的地方就是：
> 带宽、延迟
>> 其中优化延迟当中有：
（1）浏览器阻塞
（2）DNS查询
（3）建立链接
### http1.0（1996）与http1.1（1999）的区别
（1）缓存处理
> HTTP1.1则引入了更多的缓存控制策略，如Expires 

（2）带宽优化及网络连接的使用
> 请求头引入了range头域，它允许只请求资源的某个部分

（3）错误通知的管理
> 新增了24个错误状态响应码

（4）Host头处理
> 一台服务器有多个虚拟主机，所以新增支持Host头域

（5）长链接
> 默认开启Connection： keep-alive，减少请求创建链接的缺点
### http2.0（2015）
（1）新的二进制格式
> 因为多样性、且不稳定，最后制定使用稳定的二进制格式

（2）多路复用
> 每一个request对应一个id，这样可以一个连接有多个request

（3）header压缩
> encoder来减少需要传输的header大小，并且cache一份header（缓存）

（4）服务端推送
> 具有服务器端发推送的功能