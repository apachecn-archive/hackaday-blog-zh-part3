# IceSL 是一个很酷的切片机

> 原文：<https://hackaday.com/2017/11/10/icesl-is-a-cool-slicer/>

3D 打印机的机械和电子部分对成功至关重要，切片软件也是如此。Slic3r 和 Cura 可以说是最受欢迎的，它们如何控制你的打印机与你能得到的结果有很大关系。有很多其他的免费和付费的切片器，但是很难真正深入其中的每一个，看看它们是否真的比你现在使用的更好。如果你对 IceSL 的性能感兴趣——这是一款适用于 Windows 和 Linux 的免费切片器——[DIY 3d tech]有一个[视频评论](https://www.youtube.com/watch?v=nCDEOsgAt3g)，可以帮助你决定是否要尝试一下。你可以看下面的视频。

IceSL 有几个模块，实际上可以在 Lua 中做类似 OpenSCAD 的建模，所以理论上，你可以在这个工具中做任何事情。然而，这篇综述只关注切片方面。除了桌面客户端版本，你还可以使用一些功能[在线](http://shapeforge.loria.fr/slicecrafter/)(尽管在我们的 Linux 机器上，即使没有插件，它也不能与最新的 Chrome beta 一起工作；不过，火狐运行得很好。

评论中令人兴奋的一件事是，切片器允许您更改每个层的设置，它可以进行自适应切片，根据您要打印的对象选择层设置。当然，其他切片器也可以做类似的事情，但是，例如，Slic3r 要求您在 CAD 程序中创建立方体，以定义您希望附加设置应用的位置(修改器网格)。

每一层的设置都很方便。例如，您可能希望填充对象的底部，而不是顶部。床上更高的温度也很容易做到这一点。有一个单独的工具以切片器-不可知论者的方式来做这件事，但是将它内置肯定更好。如果你太执着于使用一个不是你自己创造的工具，也许你愿意[编写你自己的切片器](https://hackaday.com/2017/03/01/diy-3d-slicer-is-a-dynamo/)。

 [https://www.youtube.com/embed/nCDEOsgAt3g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/nCDEOsgAt3g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

