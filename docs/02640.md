# 吉他拾音器绕线机的数控升级

> 原文：<https://hackaday.com/2016/06/18/cnc-upgrade-to-guitar-pickup-winding-machine/>

用手给感应吉他拾音器上弦的想法几乎是不可想象的。它使用极细的金属丝，是一个重复、费力的过程，但仍需要一定的精度。这是自动化的主要候选，虽然[大卫·吉罗尼]确实做到了，但他对他的早期版本并不完全满意。他现在有了新的 CNC 版本，功能更加全面，使用 ATMega8 微控制器。

[Davide Gironi]的[以前的版本](http://davidegironi.blogspot.ca/2014/05/a-pickup-winding-machine-built-on.html)负责上弦和计算圈数，但它仍然是一个依赖人类操作员的辅助手动系统。新的升级包括一些更完全自动化过程所必需的功能，如焊线张紧器、焊线引导和横移机构(由从损坏的扫描仪中回收的部件制成)，以及当达到正确的圈数时自动停止。

![guitar_pickup_winding_sample_microscope](img/e8c65f35ad1f019f3267c43272704461.png)

所有小而重要的细节都包含在建造中，例如使用塑料和毛毡处理电线——极细的电线被一层非常薄的涂层绝缘，必须小心不要刮坏它。此外，还需要计算横动机构必须将导线器移动多远，以便将新导线放置在先前放置的线匝旁边(考虑到卷绕速度，卷绕速度可能在变化)，并且平滑地进行这一操作，使得系统不需要对每一层卷绕进行加速和减速。

该系统仍然使用按钮和 LCD 进行手工编程，但[Davide Gironi]表示，下一个版本将使用 UART，以便与计算机通信(并通过计算机进行配置),这为轻松处理多种缠绕模式打开了大门。你可以在下面看到当前版本的视频。

 [https://www.youtube.com/embed/qwnwmKib3Ow?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/qwnwmKib3Ow?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



缠绕吉他拾音器已经产生了许多半自动化的解决方案，比如基于旧缝纫机的缠绕工作站。看到人们想出什么来让事情更上一层楼是非常有趣的。