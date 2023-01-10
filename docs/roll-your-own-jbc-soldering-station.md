# 推出您自己的 JBC 焊台

> 原文：<https://hackaday.com/2017/11/06/roll-your-own-jbc-soldering-station/>

[Marco Reps]用大量热物质焊接一些电路板，发现他常用的烙铁无法胜任这项任务。他注意到一些他喜欢的专业 JBC 焊台，但他不喜欢其价格。即使是入门级的 JBC 站也要 500 美元左右，而且价格还会上涨。他决定[建造自己的](https://www.youtube.com/watch?v=GYIiOkr6x9o)，但是[确实花了一段时间才完成](https://www.youtube.com/watch?v=cYgjcDbSyRE&t=15s)。你可以在下面看到两个关于这个项目的视频。

你怎么能建立自己的焊接站，还声称这是一个 JBC？[马尔科]注意到熨斗的真正性能来自尖端——JBC 称之为弹药筒。此外，手柄提供了良好的人体工程学设计。你可以从 JBC 买到比一个加油站便宜得多的齿尖和齿柄。你只需要增加电子设备就能让它正常工作。

带着手柄和弹药筒，他开始制造电源。该墨盒有一个加热器和一个传感器，所以一个简单的 PID 控制器应该做的把戏。然而，[Marco]发现连线与其他技巧有些不同，需要一些特殊的技巧。

他从 Maxim 热电偶芯片开始。不幸的是，Maxim 部分不适合正确类型的热电偶，并且在处理尖端接地时有困难。他还发现额定功率为 250 瓦的墨盒需要大约 40 伏才能达到这个功率水平。

设计还不止这些，[Marco]介绍了所有细节。他最初的设计使用了三端双向可控硅开关，尽管他不喜欢这种性能。在第一个视频结束时，他已经有了一个围绕着一个非常大的变压器的工作原型。

第二个视频讲述了他所做的改变，并将设备包装成比原型更实用的东西。他最初试图用固态继电器取代三端双向可控硅开关元件，但没有成功，但他最终推出了自己的高效场效应晶体管固态继电器。

这让我们想起了使用 [Hakko 硬件](https://hackaday.com/2016/01/05/diy-hakko-soldering-station/)的相同技巧。就此而言，我们也看到人们使用更好的小费。

 [https://www.youtube.com/embed/GYIiOkr6x9o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/GYIiOkr6x9o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/cYgjcDbSyRE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/cYgjcDbSyRE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

