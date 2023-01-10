# 一个木制的，CD 步进画符

> 原文：<https://hackaday.com/2015/10/27/a-wooden-based-cd-stepper-scribbler/>

[Rohit Gupta]带着一个由废弃的 CD 驱动器和一个旧的 RC 伺服系统制成的绘图仪回来了。[Rohit]正致力于黑客创造数控机器，并与世界分享他的活动。他的 CNC 设计需要回收的步进电机，所以他首先[制造了一个测试设备](http://rohitg.in/2015/09/24/CNCsnMe1/)。你不得不佩服他对语言的运用。他将他的绘图仪项目命名为“Sketchy ”,而他的电机测试仪则被命名为“Easy Peasy”。

在废品堆里找到一些光驱后，他轻而易举地把它们拆下来进行测试。框架的原材料来自一个空调设备的木箱，但他不只是开始切割它。不，首先他用 CAD 创建计划；这才是你不得不佩服的一招。

随着步进机的测试工作，基础建设正在进行中，他转移到控制系统。最初使用 MSP430 演示硬件。这种方法奏效了，但是在硬件设计中发现了一个缺陷。将笔直接连接到伺服喇叭上，当笔旋转离开绘图位置时，它将绘制一条长线。

修复是一个替代的伺服设置，它将笔抬起来，而不是旋转它。但这表明绘画表面并不光滑。这支笔总是找不到地方，或者被发现并毁坏。弹簧笔的使用解决了这个问题。成功！

一个进一步的变化是从 MSP430 移植到 Arduino Pro Mini，以便使用 GRBL 库而不是 g 代码生成器，g 代码生成器的性能令人质疑。因为他非常喜欢 Hackaday，所以他对 Sketchy 最终版本的第一次尝试就是我们的标志，在休息后的视频中显示。

当我们最后一次见到[Rohit]时，他已经创造了一个奇特的[PCB 尺子来测量元件](http://hackaday.com/2015/09/10/cnced-business-card/)。

 [https://www.youtube.com/embed/ASgAicTuyx4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ASgAicTuyx4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

