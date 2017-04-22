### 1.在浏览器中地址栏中输入*url*
### 2.浏览器会查找与*url*中域名相对应的*IP*地址
而*DNS*的查找过程如下：
- 浏览器缓存：浏览器会缓存*DNS*记录一段固定的时间(2~30mins)，这段时间并不是由操作系统决定的
- 操作系统缓存：如果浏览器缓存中并没有所需的记录，则浏览器会在操作系统的缓存中来继续查询
- 路由器缓存：如果*OS*中也没有会把这个查询过程延伸到路由器中，通常路由器也会有自己的缓存
- *ISP DNS*缓存：会查询ISP的*DNS*服务器的缓存
-递归搜索：*IPS*的DNS服务器开始一个在**根域名服务器**上的递归搜索，从 .com顶级域名服务器直到你输入的*url*的域名服务器，这一步图示如下：
![递归搜索示意](http://igoro.com/wordpress/wp-content/uploads/2010/02/500pxAn_example_of_theoretical_DNS_recursion_svg.png)
### 3.浏览器找到对应*IP*的*Web*服务器并发送一个*HTTP*请求
- 需要注意的是，过程详细如下：浏览器向真实*IP*地址服务器发起*tcp*链接， 三次握手，成功之后，进行*HTTP*协议会话，浏览器发送报头（请求报头），进入*web*服务器上部署的后端应用，找到与请求对应的处理
### 4.处理结束后回馈报头，将数据返回给浏览器，浏览器响应报头，200状态码，并开始下载*HTML*文档
### 5.之后就是浏览器内核(webkit ,Gecko)的工作了，绘制*DOM*树、*render*树，然后生成你所见到的页面。
>关于这一部分的详细介绍可以在这[里面](https://www.html5rocks.com/zh/tutorials/internals/howbrowserswork//)找到，文章名为《How Browsers Work: Behind the scenes of modern web browsers》。