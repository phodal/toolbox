Ops
======

Nginx Pagespeed
---

> ngx_pagespeed 是 Nginx 的一个扩展模块，主要的功能是针对前端页面而进行服务器端的优化，对前端设计人员来说，可以省去优化css、js以及图片的过程。ngx_pagespeed对nginx自身负载能力的提升基本是看不到的，甚至会因为进行服务器端的优化而使系统增加负载；但从减少客户请求数的角度去看，牺牲部分服务器性能还是值得的

主要功能如下：

 - 图像优化：剥离元数据、动态调整，重新压缩
 - CSS和JavaScript压缩、合并、级联、内联
 - 小资源内联
 - 推迟图像和JavaScript加载
 - 对HTML重写、压缩空格、去除注释等
 - 提升缓存周期
 - 以及其他config_filters

Boom
---

Boom是一个用Go语言实现的压力测试工具，就是和Apache Bench类似的工具。它提供了一个很有意思的UI，这就是我为什么推荐他的原因了：

```
1000 / 1000 Boooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooo! 100.00 %

Summary:
  Total:    1.9052 secs.
  Slowest:  0.2054 secs.
  Fastest:  0.0111 secs.
  Average:  0.1817 secs.
  Requests/sec: 524.8813
  Total Data Received:  5459000 bytes.
  Response Size per Request:    5459 bytes.

Status code distribution:
  [200] 1000 responses

Response time histogram:
  0.011 [1] |
  0.031 [10]    |
  0.050 [10]    |
  0.069 [11]    |
  0.089 [11]    |
  0.108 [10]    |
  0.128 [11]    |
  0.147 [11]    |
  0.167 [11]    |
  0.186 [295]   |∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎
  0.205 [619]   |∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎

Latency distribution:
  10% in 0.1764 secs.
  25% in 0.1841 secs.
  50% in 0.1892 secs.
  75% in 0.1942 secs.
  90% in 0.2011 secs.
  95% in 0.2024 secs.
  99% in 0.2038 secs.
```  

GoAccess
---

> GoAccess是一款开源、实时，运行在命令行终端下的web日志分析工具。该工具提供快速、多样的HTTP状态统计，可以令管理员不再纠结于统计各类数据，和繁杂的指令以及一大堆管道/正则表达式说byebye。

这生成的风格是这样的：

![GoAccess](http://toolbox.phodal.com/images/ops/goaccess-dashboard.png)


它可以轻松统计出访问概况、动态页面请求、静态页面请求（如图片、样式表、脚本等）、访客排名，访客使用的操作系统，访客使用的浏览器，来路域名，404 错误，搜索爬虫，搜索关键词等等。

而，我们所要做的只需要运行：

```shell
goaccess -f access.log
```

Fabric
---

因为我的博客是基于Django框架而开发的，我偏向于使用Python作为开发语言，所以我需要选择了Fabric作为运维工具。


> Fabric 是一个 Python (2.5-2.7) 库和命令行工具，用来流水线化执行 SSH以部署应用或系统管理任务。

更具体地说，Fabric 是：

 - 一个让你通过 命令行 执行 任意 Python 函数 的工具；
 - 一个让通过 SSH 执行 Shell 命令更加 容易 和 蟒样 的子程序库（建立于一个更低层次的库）。

Docker
---

> Docker是一个开源的引擎，可以轻松的为任何应用创建一个轻量级的、可移植的、自给自足的容器。

Jenkins
---

> Jenkins是一个用Java编写的开源的持续集成工具。Jenkins提供了软件开发的持续集成服务。它运行在Servlet容器中（例如Apache Tomcat）。它支持软件配置管理（SCM）工具，可以执行基于Apache Ant和Apache Maven的项目，以及任意的Shell脚本和Windows批处理命令。

除了将Jenkins有于持续集成环境外，我们还可以使用Jenkins来完成一些自动化的部署工作。

