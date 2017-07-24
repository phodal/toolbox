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

