CLI
===

tree
---

> tree命令可以以树形结构显示文件目录结构，它非常适合于我们给别人介绍我们的文件目录的组成框架，同时该命令使用适当的参数也可以将命令结果输出到文本文件中。

这个命令非常适用于我们写作的时候用的，如下就是toolbox下的chapters目录：

```shell
chapters
├── api.md
├── backend.md
├── chrome-plugins.md
├── cli.md
├── devices.md
├── documents.md
├── graphics.md
├── hardware.md
└── ops.md

0 directories, 9 files
```

sl
---

这是一个神奇的命令行工具，由于两个手的手速不致，我经常将ls敲成sl。而在Ubuntu上则会提示你，你是不是要安装sl，于是我就安装了。然后：

![SL](http://toolbox.phodal.com/images/cli/sl-tool.jpg)

每次我敲错命令的时候，都会有这个神奇的火车头出现，火车头动的期间就只能等它完成。每次这个时候，就说明我们需要休息。

cURL
---

cURL利用URL语法在命令行方式下工作的开源文件传输工具。它是一个很常用的命令，也可以支持文件上传和下载。

``` shell
curl -I -s -A 'Googlebot' www.phodal.com
HTTP/1.1 200 OK
Server: mokcy/0.17.9
Content-Type: text/html; charset=utf-8
Connection: keep-alive
Vary: Accept-Encoding
Vary: Accept-Language, Cookie
Content-Language: en
X-UA-Compatible: IE=Edge,chrome=1
Date: Thu, 09 Apr 2015 14:39:11 GMT
X-Page-Speed: Powered By Phodal
Cache-Control: max-age=0, no-cache
```

``` shell
curl --data "_method=PUT&led1=1&sensors1=22&sensors2=12&temperature=14" http://b.phodal.com/athome/1
```
