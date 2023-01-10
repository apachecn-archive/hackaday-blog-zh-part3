# 机器人用系列弹性致动器介绍

> 原文：<https://hackaday.com/2015/12/03/an-introduction-to-series-elastic-actuators-for-a-robot/>

也许现在最有趣的 YouTube 频道之一是[詹姆斯·布鲁顿的]XRobots.co.uk 频道——他是一名道具制造商、玩具制造商——正如他的网站所暗示的，是一名机器人专家。把它们放在一起，看着他让你的一些童年梦想实现。他目前正在创作一个现实生活中的机器人奥创，现在他正在摆弄[系列弹性致动器](http://www.youtube.com/watch?v=-deICvHVo5A)。

在该项目的早期，他建造了一个小型机械臂来演示他将用来控制奥创的动作捕捉套装(如果一切按计划进行，他将有一个行走机器人跟随他的一举一动！).他展示了基本的 RC 伺服电机驱动臂的工作原理，以及由于没有外部反馈，它可能不是最佳的放大方式——如果他有一个全尺寸的奥创机器人摆动它的手臂，有人可能会受伤。

这让他设计了自己的原型系列弹性致动器，使用 Arduino、电位计、一些弹性元件和齿轮 DC 电机。

当他在视频中进行分解时，这其实很容易理解。他制造的 3D 打印丝杠机构安装在一个由橡皮筋限制的连杆上。这使得系统在任何部件损坏之前有一点弹性。

关节上的电位计测量臂的角度，第二个线性致动器测量电机安装沿臂的位置。在空载情况下，Arduino 可以比较这两个电位计值来定位。引入外部反馈，Arduino 会注意到两个电位计值之间的不匹配，允许机器人停止推动(或继续推动，取决于他如何编程)。

这确实是很棒的东西——但对[詹姆斯]来说，这只是基本的 R&D，直到他建造出真正的东西。

 [https://www.youtube.com/embed/-deICvHVo5A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/-deICvHVo5A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



像往常一样，我们喜欢[布鲁顿]的视频，因为他进入了伟大的细节——感谢他强大的 3D 打印机收藏，他几乎所有的部分都是自己制作的。你见过他神奇的 BB-8 机器人模型吗？他还有一套完整的钢铁侠服装，还有一套[绿巨人版](https://www.youtube.com/playlist?list=PLpwJoq86vov8gC5fYZu6zq3JpQ0VOPQmV)——更不用说一套相当棒的 [Wii-mote 控制的 Dalek 了。](http://hackaday.com/2014/05/31/wiimote-controlled-extermination-dalek-style/)

【感谢 Llyod！]