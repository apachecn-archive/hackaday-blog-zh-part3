# 走向 DIY 翻转数字时钟

> 原文：<https://hackaday.com/2017/06/18/towards-diy-flip-digit-clocks/>

七段显示器和 Nixies 是一回事，但所有古董显示技术的国王必须是机电翻转点。这些显示器通常出现在火车站，或者很少出现在旧的公共汽车线路上，是一系列物理磁盘，一边是黑色的，另一边是亮的，在电磁铁的帮助下来回“翻转”。它们价格昂贵，令人印象深刻，驾驶它们是一种痛苦，但是它们看起来棒极了。

如果你知道在哪里可以买到新的 flip dot 显示器，那么[sjm4306]有了用廉价材料制作自己的想法。这可能只是一个原型，[但是我们说他已经成功了](https://www.youtube.com/watch?v=57SxC-MEEaY)。他有七个翻转段显示器的工作方式，他使用的技术意味着建造自己的显示器不会太贵。

[sjm]不是建立一个翻转点矩阵，而是建立一个机械的七段显示器。每个片段都是用黑色 PLA 3D 打印的，并通过穿过片段长度的细线“轴”安装到一块纸板上。正常的翻转点使用电磁体将每个点从一种状态改变到另一种状态，[sjm]在片段的一端安装了一个非常小的振动传呼机马达。当轻触开关 h 桥的一半被激活时，该段翻转到前面。当 h 桥的另一半被激活时，该段翻转回来。

现在，这种硬件处于“极端原型”阶段，但迄今为止的结果令人鼓舞。[sjm]已经设计了单段‘模块’。电子设备的计划包括用于每个段的两个微控制器引脚的光耦合器和用于每个单独数字的簧片继电器。对于四位数显示器，这些翻转数字只需要 18 个 I/O 引脚。

你可以在下面查看[sjm4306]关于这个项目的视频。有点长，但是看那些东西翻转！

 [https://www.youtube.com/embed/57SxC-MEEaY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/57SxC-MEEaY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

