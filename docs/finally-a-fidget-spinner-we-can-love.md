# 最后，我们可以爱一个坐立不安的旋转

> 原文：<https://hackaday.com/2017/11/26/finally-a-fidget-spinner-we-can-love/>

坦率地说，我们对坐立不安的纺纱工的流行感到困惑。毕竟，我们可以很好地翻转墨水笔。然而，[MakersBox]刚刚向我们推销了他所谓的[极客 spinner](http://www.instructables.com/id/Geek-Spinner/)。事实上，旋转器实际上是一个 PCB，上面有零件，可能已经足够酷了。然而，该旋转器还设置了一个视觉暂留 LED，可以在旋转时显示 12 个字符的文本。因为该板很简单，并且使用通孔元件，所以对于初露头角的年轻黑客来说，这将是一个很好的项目。下面可以看到一个视频。

这些说明也适用于尝试第一个项目的人。如果你知道如何焊接和插入 DIP IC，你可能会发现你会略读，但这是非常简单的。一侧的 8 个 led 由 ATTiny CPU 控制，您可以用 Arduino 对其进行编程。旋转器有一个霍尔效应传感器和一个磁铁来计算旋转的索引位置，这对显示文本至关重要。

虽然电路板试图平衡组件，但电池一侧显然有点重。建议是使用一些硬件或焊料在侧面增加一些重量。说到焊接，中间的轴承焊接到 PCB 上。这需要很大的热量，所以也许你最终可以使用爸爸的焊枪，它一直在你的长凳下积灰。

我们喜欢提供的极坐标图来帮助您为自己的消息设置代码。该文本暗示有一张填写了这些图表之一的图片，但我们认为他忘了包括那张图片。然而，如何使用它是足够清楚的，并且它将使你自己的文本或 spinner 可以产生的任何设计变得非常容易。

顺便说一下，这不是第一个视点微调器。[MakersBox]对他看到或借鉴的项目有一套很好的致谢，但他提到的另一个项目使用了表面贴装。诚然，表面贴装现在对大多数人来说都不是问题，但一开始，坚持通孔设计可能会很好。如果你想要一个更有用的旋转器，你可以随时[制作一些音乐](https://hackaday.com/2017/09/16/fidget-spinner-gets-useful-as-midi-controller/)。

 [https://www.youtube.com/embed/BGk6_KEFtLE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/BGk6_KEFtLE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

