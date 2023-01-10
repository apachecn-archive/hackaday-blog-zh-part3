# Ocelot 街机系统说明了矢量图形的范围

> 原文：<https://hackaday.com/2018/01/09/ocelot-arcade-system-illustrates-the-scope-of-vector-graphics/>

如果没有 1983 年的崩溃，谁知道 Vectrex 系统或矢量图形游戏会走多远？如果没有这个基于市场饱和的重置按钮，游戏机大战可能会完全不同。

[Matt Carr]没有 Vectrex，但他有一台 Tektronix 465 示波器。在对爱情和文档的紧张工作之后，他还拥有了自己打造的一个闪亮的新矢量图形街机系统。它基于 dsPIC33，使用双通道 DAC 产生线框三维图形，并通过唱机输出将 X-Y 坐标发送到示波器。PIC 的内部 DAC 是针对音频的，在图形方面做得不太好，所以[Matt]使用了搭载在 PIC 的 DAC 引脚上的 TLV5618A。

豹猫不携带子弹，尽管有一天可能会。现在，改变游戏意味着摆脱困境。目前有两个可供选择:星猞猁，一个可怕的飞行射击游戏，在那里你可以拯救猫的数量，和 Mattsteroids，这正是它的声音。世界上只有一只豹猫，虽然它是非卖品，但如果你想复制它，[马特]有[非常棒的技术文档](http://www.mrdictionary.net/ocelot/technical_prototype_2016.htm)。有一件事你可能无法复制，那就是他为《豹猫》制作的经典广告，广告将在休息后播放。

难道没有‘范围’吗？你可以用 FPGA 在 CRT 上制作矢量图形。

 [https://www.youtube.com/embed/bBtuDdRtv20?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/bBtuDdRtv20?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

