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
