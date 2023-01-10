# 你不需要成为托尼·斯塔克也能买得起这个手柄

> 原文：<https://hackaday.com/2018/03/09/you-dont-need-to-be-tony-stark-to-afford-this-hand-controller/>

为了证明胶带真的可以做任何事情，[StudentBuilds]用它把手套变成了可以工作的控制器。公平地说，还有更多的比特，包括涂有铅笔石墨和锡箔的纸张，这形成了一个可变电阻器，你可以通过 Arduino 模拟输入读取。你可以在下面的视频中看到整个过程。

源代码在这一点上很简单——最终，他计划用控制器控制一只机器人手，但那是以后的事了。然而，在描述中没有承诺链接到代码，所以你必须冻结帧和类型。然而，这非常简单，只需读取模拟引脚值，即可确定每个手指的具体值。

版本有点小问题。首先，所有传感器读取最大值(1023)。这就需要将固定电阻改变到更高的值。此外，请务必阅读屏幕上的注释，因为原始原理图有一个小错误，已用注释进行了更正。分压器的一端需要达到 5 V，原理图显示两端都接地。

这会非常准确吗？不。如果你构建多个，它甚至是不可重复的，校准甚至可能会随着年龄而改变。不过，你可以拿一些废料做点什么，这很酷。此外，自制传感器的方法可能会激发你的想象力，制作其他基于铅笔的传感器。

如果你想要更机械的东西，试试乐高玩具。如果你想不出戴着这样的手套想要控制什么，也许[可以试试音乐](https://hackaday.com/2016/01/12/second-skin-synth-fits-like-a-glove/)。

 [https://www.youtube.com/embed/kFkyxxeKEOM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/kFkyxxeKEOM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

