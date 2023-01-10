# 毫米波雷达跟踪手势

> 原文：<https://hackaday.com/2017/01/24/millimeter-wave-radar-tracks-gestures/>

如果我们相信科幻小说——从*少数派报告*到*钢铁侠*，到*特克瓦尔——*电脑界面的未来属于手势。有许多方法可以读取手势，尽管它们通常需要某种手套或红外发射器，这使得它们不太方便(没有双关的意思)。

有些运动，如 Leap Motion，由于各种原因并没有受到欢迎。Soli(来自谷歌高级技术和项目组)是一个使用毫米波雷达的手势传感器。该设备发射宽无线电波束，然后收集包括返回时间、能量和频移在内的信息，以了解该领域中物体的位置和运动。你可以在下面看到一段关于这款设备的视频。

你自然会想到用光学技术来看手势(和人类一样)。然而，雷达也有一些优点。例如，它对光不敏感，可以通过塑料材料传播。Soli 系统工作在 60 GHz，传感器使用调频连续波(FMCW)和直接序列扩频(DSSS)。包含多个波束成形天线意味着该设备没有移动部件。

显然，这是最先进的设备，还没有现成的。但是好消息是，英飞凌公司计划在今年的某个时候将这种传感器推向市场。计划中的早期应用包括智能手表和扬声器，它们都使用该技术对手势做出响应。

有趣的是，Soli 处理堆栈应该是雷达不可知的。我们还没有研究它，但我们想知道你是否可以使用堆栈来处理其他类型的传感器输入，这可能对黑客更友好？除此之外，我们很想看看我们的社区能想出什么办法来解决同样的问题。

我们已经看到 Raspberry Pi 子板(ok，hats)可以识别用来控制电视的手势。如果你有什么想法的话，我们甚至已经用声纳建立了一些[原始手势感应。你打算用 Soli 吗？还是滚动自己的超级手势传感器？在](http://hackaday.com/2015/12/13/arm-based-gesture-remote-control/) [Hackaday.io](http://hackaday.io) 上让我们知道并记录你的项目。

 [https://www.youtube.com/embed/0QNiZfSsPc0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/0QNiZfSsPc0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

