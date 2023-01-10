# 闻到了吗？是时候了。

> 原文：<https://hackaday.com/2018/01/30/smell-that-its-time/>

蒸汽朋克很美。裸露的金属和原始外观的人工制品在视觉上吸引了制造商和工程师的大脑。制造商们在过去的十年里一直忙于建造这种主题的时钟，因为嘿，每个人都需要一个时钟。[机身]组装了一个[蒸汽朋克钟，为它的整点报时](https://hackaday.io/project/33750-steam-clock)释放实际的蒸汽(实际上是蒸汽油烟)。多酷啊。

时钟是围绕着摩托罗拉 68HC08 的 [Conrad C-Control Unit](https://de.wikipedia.org/wiki/C-Control) ( [译](https://translate.google.com/translate?sl=auto&tl=en&js=y&prev=_t&hl=en&ie=UTF-8&u=https%3A%2F%2Fde.wikipedia.org%2Fwiki%2FC-Control&edit-text=))设计的，[机身]用 BASIC 编写系统的例程。与许多使用谢妮电子管的蒸汽朋克钟不同，这款钟使用 4 个 Numitron 显示器来显示小时和分钟。采用模拟表盘显示秒，并由 PWM 信号驱动。RTC 模块的缺失并不明显，直到我们看到 BOM 包括一个 DCF77 接收器。对于外行人来说，DCF77 是一个长波时间信号和标准频率无线电台，位于德国的 Mainflingen。如果你在该地点 2000 公里范围内的任何地方，你可以免费接收 24 小时报时信号，如果你打算制作一个收音机闹钟，这是一个极好的选择。

蒸汽/烟雾发生器是一个子项目。除了实际的发电机之外，定制机器被设计成具有单独的储油器和泵，以便系统不会很快耗尽燃料。显然[机身]做了他的功课，这在他的项目日志中有简单的解释。最终的设计有一个黄铜管作为主要的加热装置，同时也作为出口室。油从黄铜管中的加热丝下抽出，多余的液体流回油箱。一根镍铬合金丝充当灯丝，将液体蒸发成气体。传感器确保油箱和蒸汽管中的油位。伺服电机和风扇增加了打开排气雨盖的效果，一个小 LED 有助于照亮排气，以完成真实蒸汽的印象。

该项目是一个简单而有效的实现的很好的例子，对于那些对 Numitron 电子管感兴趣的人来说，可以看看这个主题为的教程。当然，还有[巨型电动机械钟](https://hackaday.com/2017/07/04/steampunk-inspired-art-clock/)，供那些想看更大型艺术品的人使用

 [https://www.youtube.com/embed/5RXw3Jb6DJg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/5RXw3Jb6DJg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

