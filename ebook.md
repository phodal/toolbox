
文档篇
===

![Documents](http://toolbox.phodal.com/images/documents/documents.png)

Pandoc
---

> Pandoc是一个标记语言转换工具，可实现不同标记语言间的格式转换，堪称该领域中的“瑞士军刀”。

可以将 markdown、 reStructuredText、 textile、 HTML、 DocBook、 LaTeX、 MediaWiki markup、 TWiki markup、 OPML、 Emacs Org-Mode、 Txt2Tags、 Microsoft Word docx、 LibreOffice ODT、 EPUB、 Haddock markup

转化为

XHTML、 HTML5、 以及HTML幻灯片Slidy， S5，或者DZSlides、Microsoft Word docx、 OpenOffice/LibreOffice ODT、 OpenDocument XML、EPUB、DocBook、 GNU TexInfo、 Groff man pages、LaTeX、 ConTeXt、 LaTeX Beamer slides、PDF via LaTeX、Markdown、 reStructuredText、 AsciiDoc、 MediaWiki markup、 Emacs Org-Mode、 Textile

上图

![Pandoc](http://toolbox.phodal.com/images/documents/pandoc.png)

我最常用的就是：将md转化为workd及pdf。我的毕业论文及之前的几本电子书都是这么做的，它是一个命令行工具，安装方式：

 - Windows: choco install pandoc
 - Ubuntu/CentOS/OpenSUSE: apt-get intall pandoc 或者 yum install pandoc
 - Mac OS: brew install pandoc

使用方式如下：

      pandoc fullstack.md -o fullstack.docx

如果要转为PDF，则需要另外的一个工具——LaTeX

Graphviz
---

> Graphviz （英文：Graph Visualization Software的缩写）是一个由AT&T实验室启动的开源工具包，用于绘制DOT语言脚本描述的图形。它也提供了供其它软件使用的库。

简单的来说，就是将代码转换为图形:

![Graphviz](http://toolbox.phodal.com/images/documents/graphviz-example.png)

它让我最惊讶的是DOT语言，简直是以我们平时的用法来定义的。上面的图形的代码类似于这样的：

    home->products->widgets

又是一个让人惊呆的黑科技，这才是人类应该使用的语言。它可以支持PostScript，PDF，SVG，PNG等一系列的格式，用法

     dot -T png phodal.dot -o phodal.png

简单、粗暴到没有朋友。

ImageMagick
---

> ImageMagick (TM) 是一个免费的创建、编辑、合成图片的软件。它可以读取、转换、写入多种格式的图片。图片切割、颜色替换、各种效果的应用，图片的旋转、组合，文本，直线，多边形，椭圆，曲线，附加到图片伸展旋转。

来自重点：可以支持超过两百多种格式。It can read and write images in a variety of formats (over 200) including PNG, JPEG, JPEG-2000, GIF, TIFF, DPX, EXR, WebP, Postscript, PDF, and SVG.

它提供了一个命令行工具叫：``convert``，这可以自由地转换图片的形式，如：

    convert image.jpg image.png

还可以加各种效果，如：

![ImageMagick](http://toolbox.phodal.com/images/documents/gausisan.jpg)

顺便做个介绍：上面的这个人叫瑞典模特儿莱娜·瑟德贝里，是在刊于1972年11月号《花花公子》杂志上的一张裸体插图照片的一部分。**她的脸部与裸露的肩部已经变成了事实上的工业标准。**

又是一个简单、粗暴到没有朋友的工具。

TeX 和 Latex
---

TeX是由是一个由美国计算机教授高德纳（Donald Ervin Knuth）编写的功能强大的排版软件。顺便推荐一下他写的一本书：《计算机程序设计艺术》。因为：

> 高德纳最早开始自行编写TEX的原因是当时十分粗糙的排版水平已经影响到他的巨著《计算机程序设计艺术》的印刷质量。他以典型的黑客思维模式，最终决定自行编写一个排版软件：TEX。他原本以为他只需要半年时间，在1978年下半年就能完成，但最终他用了超过十年时间，直到1989年TEX才最终停止修改。

这直接让我想起Martin Fowler在写《领域特定语言》里好像也是用DSL。Tex的最大优点是可以写出下面的这本复杂的公式：

![formular](http://toolbox.phodal.com/images/documents/formular.jpg)

LaTeX 建立在 TeX 之上的工具，它在TeX的基础上大大改善了易用性。对了，如果只是一般的用途的话，就没有必要拿去装逼了~。

它也是工作于命令行上的工具。

Jupyter Notebook
---

Jupyter Notebook使用浏览器作为界面，其前身是Ipython Notebook，Ipython3.0之后新建为Jupyter项目。它支持Markdown、Python语言交互、R语言交互、图形显示、运行时间分析、LaTex公式，对于交互编程、数据分析和数据可视化非常有用。

![Jupyter](http://toolbox.phodal.com/images/documents/Jupyter.png)

**安装（使用pip）**

    $ pip install jupyter

**运行**

    $ jupyter notebook

官网：[Jupyter](https://jupyter.org/)


Gitbook
---

Gitbook是一个命令行工具(node.js库)，可以把你的Markdown文件汇集成起来，生成一个静态网站，也可以输出为PDF等多种格式。

![gitbook](http://toolbox.phodal.com/images/documents/gitbook.jpg)

**安装（使用npm）**

    $ npm install gitbook-cli -g

**使用**

    $ gitbook init ＃ 初始化书籍目录
    $ gitbook serve ＃ 运行

官网：[Gitbook](https://www.gitbook.com/)

图形工具篇
===

在上一篇《全栈工程师的百宝箱：黑魔法之文档篇》我们介绍了一些文档工具，今天让我来分享一下，我常用的一些图形工具。

## 流程图：Graphviz

说到流程图还是再次提及一下，我们之前说到的**Graphviz** 。

> Graphviz （英文：Graph Visualization Software的缩写）是一个由AT&T实验室启动的开源工具包，用于绘制DOT语言脚本描述的图形。它也提供了供其它软件使用的库。

它的主要特点是代码生成图像，并且足够的简单。

在我的那个“Web Developer 成长路线图”(GitHub: [https://github.com/phodal/developer](https://github.com/phodal/developer))里，就是用这个工具生成下面这个复杂的图形。

![tree.png](http://toolbox.phodal.com/images/graphics/tree.png)

而其代码特别简单——和我们平时表达的手法是一样的，即：

```
"包管理" -> "包发布" -> "自动部署"
"CLI" -> "部署"
"脚本语言(Bash,Perl,Ruby,Python etc)" -> "部署"
"脚本语言(Bash,Perl,Ruby,Python etc)" -> "构建"
"*nix" -> "软件编译" -> "部署"
"构建" -> "软件编译"
```

 Graphviz有一个大的优点和弱点是：自动生成，导致画线的时候很出现出问题。接着，我们就来看看手动画线的例子。

## 流程图： Visio vs Dia vs OmnIGraffle

在Windows世界里，在这一类的工具里面最常见的算是Visio:

![MS-Visio-flowchart.png](http://toolbox.phodal.com/images/graphics/visio.png)

遗憾的是，它并不支持在Mac OS上使用。而且，它并不在我购买的Office 365套装里。

在Mac世界里，最好的工具算是OmniGraffle，就是很贵——我们平时使用的是公司的Mac电脑，使用盗版软件是有法律风险的。

![Omnigrafflescreen.jpg](http://toolbox.phodal.com/images/graphics/omnigraffle.jpg)


在GNU/Linux世界里，我们使用Dia。

> Dia 是开放源代码的流程图软件，是GNU计划的一部分，程序创立者是Alexander Larsson。Dia使用单一文件界面模式，类似于GIMP与Inkscape。 Dia将多种需求以模块化来设计，如流程图、网络图、电路图等。各模块之间的符号仍是可以通用的，并没有限制。

![dia_screenshot.png](http://toolbox.phodal.com/images/graphics/dia_screenshot.png)

顺便安利一下，我最喜欢的操作系统OpenSuSE——简洁、尾长、绿色。

![opensuse.jpg](http://toolbox.phodal.com/images/graphics/opensuse.jpg)

OpenSuSE在KDE桌面下效果最赞了——因为KDE和OpenSuSE都是德国制造。总的来说，会比Debian系的Debian和Ubunt，及RetHat系的CentOS及Fedora稳定、漂亮。

令人遗憾的是这三个工具，我都用不了。Mac对X Windows的支持不是一般的差，于是我就需要别的替代工具。

## 在线流程图：Processon

这个工具还是相当好用，至少是在GxFxW内比较快——我之前使用过Creately、draw.io、Gliffy等等的一些工具，只是随着版图的扩展，很多地区都已经“xx”了。

![tlok.jpg](http://toolbox.phodal.com/images/graphics/tlok.jpg)

不过遗憾的是：他们没有给我广告费。

> ProcessOn是一个在线协作绘图平台，为用户提供最强大、易用的作图工具！支持在线创作流程图、BPMN、UML图、UI界面原型设计、iOS界面原型设计等。

同样的，在我的那个“Developer进阶书单”（GitHub: [https://github.com/phodal/booktree](https://github.com/phodal/booktree))中，就是用这个工具画出规规矩矩的线。

![BookTree.png](http://toolbox.phodal.com/images/graphics/BookTree.png)

并且，它还是跨平台的。

## 各种图： Word和Excel

由于翻译和写书的需要，我成了一个Office 365订阅用户。于是发现在Word等一系列的Office工具中，自带了一个SmartArt的工具：

![smart-art.png](http://toolbox.phodal.com/images/graphics/smart-art.png)

可以画出很多很有意思的图形，比如：

![编程之路.png](http://toolbox.phodal.com/images/graphics/program_road.png)

又或者是：

![growth-lob.jpg](http://toolbox.phodal.com/images/graphics/growth-lob.jpg)

分分钟就能画一个的节奏。

## 脑图： XMind

我想这个一般人都是知道的。

> XMind思维导图软件被著名互联网媒体Lifehacker评选为“最佳头脑风暴和思维导图工具”及”最受欢迎的思维导图软件”。

它有一个很大的优点是使用了全球最先进的Eclipse RCP 软件架构，支持跨平台使用。它有一个很大的缺点是使用了全球最先进的Eclipse RCP 软件架构，导致了有点卡。

相比于流程图什么的，它只适合做脑图。

![banner_index.png](http://toolbox.phodal.com/images/graphics/banner_index.png)

如果你还在使用Eclipse，那么你应该试试Intellij IDEA了。

## 各种图：D3.js

> D3.js（D3或Data-Driven Documents）是一个用动态图形显示数据的JavaScript库，一个数据可视化的工具。

与上面的工具相比，这个工具可能没有那么方便。但是，作为一个数据可视化工具，它不仅仅可以做出各种炫酷的图形。

还可以做出一个技能树：

![sherlock.png](http://toolbox.phodal.com/images/graphics/sherlock.png)

这个项目的GitHub见：[https://github.com/phodal/sherlock](https://github.com/phodal/sherlock)

## 地图：Leaflet

> Leaflet 是一个为建设移动设备友好的互动地图，而开发的现代的、开源的JavaScript 库。

虽然它与上面的图形没有啥关系，但是它带了一个图字啊。与Google Map原生的API，或者OpenStreet相比，它最大的优点是对移动设备支持好。

并且，它也是一个可以根据数据（GEOJSON，地理数据）生成图形的工具。

![vmap.jpg](http://toolbox.phodal.com/images/graphics/vmap.jpg)

Chrome插件篇
===

Chrome DevTools
---

在我所用过的这些前端工具里，最常用、实用的就属Chrome自带的DevTools。通常情况下，我们只需要使用这个工具就可以完成大部分的工作了。

![Chrome DevTools](http://toolbox.phodal.com/images/fe-plugins/dev-tool.jpg)

每个前端工程师，都应该好好学习如何去使用Chrome DevTools。当然，这并不是一篇详细的关于Chrome DevTools的介绍——相关的内容足够写一本书了。除了正常的Debug功能，它可以模拟移动设备，模拟网络、模板分辨率、模拟，并在HTTP请求中带上相应的User Agent方便我们调试。

Open SEO Stats
---

顾名思义这是一个SEO状态查询工具，它可以让我们查看网站的SEO相关信息。也是一个非常棒的反诈骗软件，因为一个好的网站的Alexa Traffic Rank、PR以及Pages indexed（索引数）等等都会相对较高。

![Open SEO Stats](http://toolbox.phodal.com/images/fe-plugins/seo-stats.jpg)

除了基本的SEO状态显示，它还提供了一些有效的工具，来帮助我们优化页面的SEO。如在Page Info里，会罗列出页面的相关标签是否完整。在Links Stats里，会帮我们检查页面的外链情况等等。

PageSpeed Insights
---

这是Google的PageSpeed Insights的插件版（网页版见： [https://developers.google.com/speed/pagespeed/insights/](https://developers.google.com/speed/pagespeed/insights/)），一个非常棒的网页优化工具，有了它就可以让我们轻松对网页进行优化。我们所需要做的事情就是点击“分析”按钮，然后就坐等他分析完成。

如下就是我博客的一个分析结果：

![PageSpeed Insights](http://toolbox.phodal.com/images/fe-plugins/pagespeed.jpg)

总体分数98分，看来我针对这个所说的东西进行优化的效果还不错。左边显示了我博客存在的一些问题，如：

 - 没有压缩CSS
 - 可以使用浏览器缓存
 - 需要指定缓存验证工具
 - 暂缓JavaScript解析
 - 将查询字符从静态资源中删除

等等的几个问题——这些已经都是小问题了。所以他们的重要等级是“低”，一般来说如果有一个等级是“高”整个评分就会特别低。

除此，我们还可以使用命令行工具来对你的网页进行测试。

[https://github.com/addyosmani/psi](https://github.com/addyosmani/psi)

安装：

``` shell
$ npm install --global psi
```

只需要执行下面的命令即可：

``` shell
psi http://www.example.com/
```

如我的博客的结果:

``` shell
--------------------------------------------------------

URL:       phodal.com
Strategy:  mobile
Speed:     90
Usability: 96

CSS size                                   | 30.04 kB
HTML size                                  | 11.8 kB
Image size                                 | 41.08 kB
JavaScript size                            | 28.07 kB
CSS resources                              | 1
Hosts                                      | 2
JS resources                               | 1
Resources                                  | 5
Static resources                           | 3
Total size of request bytes sent           | 695 B

Leverage browser caching                   | 1.5
Main resource server response time         | %
```

再依据不同的结果对网页进化优化，不过它有一个前提是它并不适合SPA（单页面）应用。

Postman
---

我相信这个软件，搞过Web开发的人都听过。

![Chrome Postman](http://toolbox.phodal.com/images/fe-plugins/postman.jpg)

它是一款功能强大的网页调试与发送网页HTTP请求的Chrome插件。总之，就是我们可以在浏览器上执行GET、POST等等的测试。在调试远程API的时候很有用，一般在调试本地API的时候，我都是用jQuery的。

同样的，你仍然可以使用命令行工具来测试它，即[Newman](https://github.com/postmanlabs/newman)。由于其没有UI，它可以运行在CI上，并编写相应的UI测试。

XPath Helper
---

这是我在写UI自动化测试的时候使用的工具，由于那是一个遗留项目，所以我们都对整体UI的布局都不是特别熟悉。并且由于业务推进的关系，我们并没有足够的时候去解决这个问题，于是就开始使用这个工具来完成工作了。

在编写的时候我们会在Console用jQuery去选定元素，然后再将其转换为XPath。接着在这个工具上尝试，如下图显示：

![XPath Helper](http://toolbox.phodal.com/images/fe-plugins/xpath.jpg)

最后，我们将会写到代码中。

ObservePoint Tag Debugger
---

这是一个可以用于调试各种Web分析工具的插件，它可以用于分析SiteCat、Google Analytics、WebTrend等发出的事件请求，并解析其数据。

![ObservePoint Tag Debugger](http://toolbox.phodal.com/images/fe-plugins/observerPoint.jpg)

Capture Webpage Screenshot Entirely
---

这是一个截图工具，可以用于截取页面长图。

外设篇
===

机械键盘
---

地球人都知道，我就不说了。

如果你问我用的是什么键盘：

 - Ducky 9008s2，大学的时候买的，家里用，紫色
 - Ducky DK2087 G2，只要399，公司用的

机械键盘手托
---

很多人光有个机械键盘，但是却没有一个与之对应的手托，我觉得还是有些可惜的。机械键盘都有着相当高的高度，这时手放上去就有些尴尬。

![机械键盘手托](http://toolbox.phodal.com/images/devices/shoutuo.jpeg)


自定义按钮的鼠标
---

对于程序员来说，复制和粘贴是很常用的操作，如果我们有一个对应的自定义按钮的鼠标的话，我们就可以光用鼠标来进行复制和粘贴了。

![Steelseries](http://toolbox.phodal.com/images/devices/steelseries.jpg)

鼠标线夹
---

我经常拿我的Macbook去玩《文明》系列的游戏，这时候我就需要鼠标了，也需要用鼠标线夹来保证我的移动不会受阻。

笔记本支架折叠
---

如果选不了一个好的椅子，那么我们就需要一个好的支架来撑起电脑到一个合适的高度。

![Steelseries](http://toolbox.phodal.com/images/devices/nexstand.jpg)

Kindle
---

Kindle，看书的人都知道。

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


自动化
===

Selenium
---

> Selenium 是一个用于 Web 应用程序测试的工具。Selenium 的测试用例直接运行在浏览器中，就像真正的用户在操作一样。与主流的 web 自动化测试框架还有 QTP，基于 Ruby 的 WATIR 等相比，Selenium 支持 IE、Mozilla Firefox 多种浏览器，支持自动录制脚本以及 Java、c#、ruby 等多种运行语言的自动生成，用例制作快捷，运行快速。相比起来 Selenium 要显得更为灵活实用。

硬件篇
===

Raspberry Pi
---

> Raspberry Pi 是一款基于Linux的单板机电脑。它由英国的树莓派基金会所开发，目的是以低价硬件及自由软件促进学校的基本计算机科学教育。

Arduino
---

> Arduino，是一个开放源代码的单芯片微控制器，它使用了Atmel AVR单片机，采用了开放源代码的软硬件平台，建构于简易输出/输入（simple I/O）界面板，并且具有使用类似Java、C语言的Processing/Wiring开发环境。

我拥有下面的一些开发板：

 - Arduino Uno，玩过都知道。通用版，可以使用一系列强大的扩展板。
 - Arduino Yun，带WiFi功能的Arduino。
 - Arduino ADK，可以使不支持USB Host功能的Android设备也可以和其它USB设备
 - Arduino Lilypad，主要用于可穿戴领域。

NodeMCU
---

> NodeMCU,是一个开源的物联网平台。 它使用Lua脚本语言编程。该平台基于eLua 开源项目,底层使用ESP8266 sdk 0.9.5版本。该平台使用了很多开源项目, 例如 lua-cjson, spiffs[5]. NodeMCU包含了可以运行在 esp8266 Wi-Fi SoC芯片之上的固件,以及基于ESP-12模组的硬件。



API
===

Moco
---

> Moco是一个简单搭建模拟服务器的程序库/工具，它是一个简单搭建 stub 的框架，主要用于测试和集成。

这个工具的目的主要是针对于前后端分离的Web应用来说，特别是基于HTTP协议的集成——Web Service、REST等。

不过如果你们不写测试的话，这个工具就没啥用。

Swagger
---

> Swagger是一种和语言无关的规范和框架，用于定义服务接口，主要用于描述RESTful的API。它专注于为API创建优秀的文档和客户端库。支持Swagger的API可以为API方法生成交互式的文档，让用户可以通过以可视化的方式试验，查看请求和响应、头文件和返回代码，从而发现API的功能。它本身就非常强大，但是Swagger框架还支持为多种流行的语言——包括JavaScript、Python、Ruby、Java、Scala等等——生成客户端代码。

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

Backend
===

Spring MVC
---

> Spring Web MVC是一种基于Java的实现了Web MVC设计模式的请求驱动类型的轻量级Web框架。

Spring Boot
---

> Spring Boot 的目的在于快速创建可以独立运行的 Spring 应用。通过 Spring Boot 可以根据相应的模板快速创建应用并运行。Spring Boot 可以自动配置 Spring 的各种组件，并不依赖代码生成和 XML 配置文件。Spring Boot 可以大大提升使用 Spring 框架时的开发效率。

Laravel
---

> Laravel是一套简洁、优雅的PHP Web开发框架。

Django
---

> Django是一个开放源代码的Web应用框架，由Python写成。采用了MVC的软件设计模式，即模型M，视图V和控制器C。

在我的博客，以及我使用的一些需要用户认证、CMS功能等等的系统里，我优先使用这个框架来完成任务。它还拥有一套设计得很不错的ORM系统，并且其还隔离了不同的系统底层。

Flask
---

> Flask是使用Python语言编写的轻量级的WebWeb应用框架。基于Werkzeug WSGI工具箱和Jinja2 模板引擎。

与Django的很大不同之处在于Flask被称之为微框架，它只有简单的核心，而其他的功能需要使用扩展来完成。这就意味着，当我们可以高度定制我们的系统，只选择我们需要的功能，并通过扩展来完成。

Express
---

> Express 是一个基于Node.js 平台的极简、灵活的web 应用开发框架，它提供一系列强大的特性，帮助你创建各种Web 和移动设备应用。

WordPress
---

> WordPress是一个以PHP和MySQL为平台的自由开源的博客软件和内容管理系统。WordPress具有插件架构和模板系统。Alexa排行前100万的网站中有超过16.7%的网站使用WordPress。到了2011年8月，约22%的新网站采用了WordPress。WordPress是目前因特网上最流行的博客系统。

Ruby On Rails
---

> 是一个使用Ruby语言写的开源Web应用框架，它是严格按照MVC结构开发的。它努力使自身保持简单，来使实际的应用开发时的代码更少，使用最少的配置。


科学
===

Octave
---

> Octave是一个旨在提供与Matlab语法兼容的开放源代码科学计算及数值分析的工具；

Numpy
---

> NumPy是Python语言的一个扩充程序库。支持高级大量的维度数组与矩阵运算，此外也针对数组运算提供大量的数学函数库。NumPy的前身Numeric最早是由Jim Hugunin与其它协作者共同开发，2005年，Travis Oliphant在Numeric中结合了另一个同性质的程序库Numarray的特色，并加入了其它扩展而开发了NumPy。NumPy为开放源代码并且由许多协作者共同维护开发。

Processing
---

> Processing是一种开源编程语言，专门为电子艺术和视觉交互设计而创建，其目的是通过可视化的方式辅助编程教学，并在此基础之上表达数字创意。

它除了制作一些酷炫的动画之外，其简单的GUI编程，还可以用于硬件端的上位机编写。

图像处理
===

GIMP
---

> GIMP (GNU Image Manipulation Program，GNU图形处理程序)是一个自由的专业图片处理软件，以GPL（GNU General Public Licence，GNU 通用公共许可协议）许可发布。 它能够用于点击数码位图，比如数码照片、扫描的图片。尽管GIMP也能够编辑矢量图形，比如SVG矢量图形，但是相对而言Inkscape、Corel Draw或Adobe Illustrator这些专门的矢量图软件的功能会更强。（因此人们通常将Inkscape与GIMP配合使用，得到更强大的工具组合）作为全功能的图像处理软件，GIMP对此领域内的专业软件如Photoshop、Corel Paint Shop Pro产生了强有力的挑战，这主要归功于GIMP众多出色的功能特性：多图层，图形缩放、调整，裁剪，颜色操作，支持众多文件格式等等。

INKSCAPE
---

> Inkscape 是开源的矢量图形编辑软件，与 Illustrator、Freehand、CorelDraw、Xara X 等软件很相似，它使用 W3C 标准的 Scalable Vector Graphics (SVG) 文件格式，支持包括形状、路径、文本、标记、克隆、alpha 混合、变换、渐变、图案、组合等 SVG 特性。它也支持创作共用的元数据、节点编辑、图层、复杂的路径运算、位图描摹、文本绕路径、流动文本、直接编辑 XML 等。它可以导入 JPEG、PNG、TIFF 等格式，并输出为 PNG 和多种矢量格式。


ImageMagick
---

> 它可以以各种格式读取和写入图像（超过200种），包括PNG，JPEG，JPEG-2000，GIF，TIFF，DPX，EXR，WebP，Postscript，PDF和SVG。使用 ImageMagick 调整大小，翻转，镜像，旋转，扭曲，剪切和变换图像，调整图像颜色，应用各种特殊效果，或绘制文本，线条，多边形，椭圆和Bézier曲线。

它可以支持以下的特性[^features]：

 - 格式转换：从一种格式转换成图像到另一个（例如 PNG 转 JPEG）
 - 变换：缩放，旋转，裁剪，翻转或修剪图像
 - 透明度：使图像的部分变为透明
 - 附加：添加形状或一帧到图像
 - 装饰：添加边框或帧图像
 - 特效：模糊，锐化，阈值，或色彩图像动画：创建一个从GIF动画图像组序列
 - 文本及评论：插入描述或艺术图像中的文字
 - 图像识别：描述的格式和图像性能
 - 综合：重叠了一个又一个的图像
 - 蒙太奇：并列图像画布上的图像缩略图
 - 电影支持：读写图像的共同使用的数字电影工作方式
 - 图像计算器：应用数学表达式的图像或图像通道
 - 离散傅立叶变换：实现正向和反向的DFT。
 - 高动态范围图像：准确地表现了从最明亮的阳光直射到最深最黑暗的阴影找到真正的幕后广泛的强度水平
 - 加密或解密图片：转换成不懂乱码，然后再返回普通图像
 - 虚拟像素支持：方便以外区域的图像像素
 - 大图像支持：读，过程，或写mebi和吉比像素的图像尺寸
 - 执行：ImageMagick的是线程安全的，利用内部算法OpenMP的功能及快速的双核和四核处理器技术提供窗口优势
 - 异构分布式处理：某些算法可以在跨越的CPU，GPU，以及其他处理器组成的异构平台音乐会执行速度提高。

它可以支持 Linux、Windows、 Mac Os X、 iOS、 Android OS 等等的系统。

如果说 Pandoc 里文档界的瑞士军刀，那么 ImageMagick 就是图形界的瑞士军刀。

上周在为 Growth 制作插图的时候，需要：1. 合并不同的图像；2. 对图片进行缩放。考虑到图片的数量差不多有 30 张左右，我决定要找一个工具。。。

这个时候就找到了 ImageMagick 中的几个命令，它居然可以完成我大部分的功能。

### 合并图像

最开始的时候，我是想合并几张图片，成如下的样子：

![SkillTree](skilltree.png)

按照我的习惯，我会打开 Photoshop，然后计算一次合成的图片的宽度。在我合成了两三张图片之后，我就累了。

搜索过后，便发现了 IMageMagick 的 ``convert`` 命令，只需要简单地执行一下：

```
convert skilltree-1.png skilltree-2.png skilltree-3.png +append skilltree.png
```

而 ``convert`` 这个命令，其所拥有的参数选项居然有 253 个，我是我在执行下面的命令后统计到的：

```
convert --help | grep "  -"|wc -l
```

它可以用来转换图像格式，调整图像大小、模糊、裁剪、去斑、抖动、绘图、翻转、加入、重新采样等等。它的功能相当的丰富，以至于我联想到我只需要有这个命令 + 一个简单的 UI，我就可以做出一个 P 图软件了。

### 批量缩放大小

在合并图像之前，我需要对图片进行缩放。同样的，我找到的工具也是 ImageMagick 中的：

```
mogrify -geometry x600 *.png
```

这里的 x600 即是图片的高度，上面的命令会将所有的 png 缩放到高度为 600 的图片。除了缩放，它还可以轻松地转换图形的格式：

```
mogrify -format jpg *.png
```

即可以将所有的 jpg 转为 png。

[^features]: 翻译源自 https://imagemagick.cn/

