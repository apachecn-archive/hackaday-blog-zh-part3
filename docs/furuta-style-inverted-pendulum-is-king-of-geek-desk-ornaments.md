# 古田风格倒立摆是极客书桌摆件之王

> 原文：<https://hackaday.com/2016/09/14/furuta-style-inverted-pendulum-is-king-of-geek-desk-ornaments/>

牛顿的摇篮被认为是最优雅的办公桌玩具。但是，当[本·卡茨]的古田摆锤在快车道上飞驰而过时，这只 20 世纪的恐龙刚刚冲出马路，掀翻了小鸟，预示着一种新的桌面装饰之王的到来。

这个 Furata 钟摆的运动非常平稳。休息之后你可以在视频中看到它的舞蹈。显然你同意这是现代工业巨头(极客)的桌面艺术品。只是不要停留在观看它的行动。最棒的部分是[Ben]整理的构建日志——这个项目几乎什么都有！

它完全重建了一个电动机。它有机械加工。有电子设备。甚至还有控制理论指南。所有这些完美地结合在一起，我们只能想象如果这样一个项目(超出了他的预算)出现在演示设备目录中，一个机械工程教授会有多么渴望。

日志的第一部分中发生了很多事情。[本]在某种程度上因[对](http://hackaday.com/2016/06/24/hobbyking-cheetah-building-running-robots-from-hobby-motors/)[小型无刷 DC 电机](http://hackaday.com/2013/04/05/electric-tricycle-build-log-is-like-hacker-crack/)了解太多(如果衡量标准是他让我们对自己的感觉有多差的话)而出名。他决定，现成的万向节电机将完全太小的扭矩和实际上令人讨厌的齿槽效应。因此，他重新缠绕电机线圈，并为它加工了一个完全不同的外壳，这样它就可以是无芯的。只是为了更好的衡量，他还扔在一个编码器，当然，重视他的定制电机驱动器。

嗯，再多一点加工，一些整理，甚至一些非常好的 Lemo 连接器之后，机械方面的工作就完成了。[第二部分跟随](http://build-its-inprogress.blogspot.lu/2016/08/desktop-inverted-pendulum-part-2-control.html)，深入探讨设备的电机控制和控制理论。他首先调整他的马达驱动器，使其与新改造的马达一起工作。接下来，他制作了自己的闭环控制器(利用摆的磁铁角度传感器工作)。避开标准的方法，只是在上面安装一个 PID 库并调整常数，直到它看起来正确为止，“没什么意思。”


 [https://www.youtube.com/embed/XKzzWe15DEw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/XKzzWe15DEw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

