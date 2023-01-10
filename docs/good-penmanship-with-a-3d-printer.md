# 用 3D 打印机书写流畅

> 原文：<https://hackaday.com/2017/01/17/good-penmanship-with-a-3d-printer/>

[克里斯·米歇尔]本来打算自己做一个绘图仪来为卡片写草书，但是意识到他也许可以用他的 3D 打印机来代替书写。但后来他找不到任何合适的软件，所以他做了在这种情况下你应该做的事情，他写了自己的 3DWriter。他甚至 3D 打印了一个支架，这样他就可以在挤出机的侧面安装一支笔。当不用作绘图仪时，他只需将笔尖缩回去。

该软件是用 C#为 Windows 编写的，可从 GitHub 上的[下载，并附有详细的文字介绍。他显然对软件提供的功能花了很多心思。选择字体后，你输入你想要打印的任何内容，然后预览以确保它看起来不错。还有一堆 g 代码设置，你可以填写，如床的大小，水平和垂直偏移的笔尖从挤出机顶端，绘图速度等。甚至还有一个选项，可以举起笔来做一次预演，这样你就可以确保它会在你期望的床上画画。](https://github.com/boy1dr/3DWriter)

代码本身非常简洁，易于理解。如果你像我们一样好奇字体文件中有什么信息，以及它是如何被翻译成 g 代码的，那么从 GitHub 页面下载源代码看看吧。[Chris]选定了一个名为 Hershey fonts 的字体集，因为它们主要是基于笔画的字体，而不是他看过的其他程序使用的轮廓字体。

这让我们想到了我们看到的那些在 hackerspace 货架上积满灰尘或被认为过时的 3D 打印机。将它们用作绘图仪赋予了它们新的生命——即使只是作为学习为 CNC 机器编写代码的一种有趣方式。这让我们想知道 2D 还能把它们用在什么地方……切割乙烯基？激光打印？有人有想法吗？

在任何情况下，看看下面的视频，看看它作为一个 2D 绘图仪的行动。作为奖励，你还会看到它使用一个 [Inkscape 插件](https://jtechphotonics.com/?page_id=2012)绘制的艺术线条。

[Chris]的黑客让我们想起了我们为 2D 见过的其他定制 g 代码编写软件。有一个软件可以给你一个简单的绘图程序来制作你的 2D 图像，然后生成 g 代码，这样你的 3D 打印机就可以将图形挤压成一个单独的塑料层。还有一种方法是[用网络摄像头拍摄一个孩子的图画，然后将其转换成 g 代码](http://hackaday.com/2016/05/11/converting-kids-hand-drawings-to-g-code/)，用激光打印机进行蚀刻。

 [https://www.youtube.com/embed/yK_YGwMRR40?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/yK_YGwMRR40?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

