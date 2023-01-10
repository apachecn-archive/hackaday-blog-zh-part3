# 8 位游戏使用我们最喜欢的集成电路和零线代码

> 原文：<https://hackaday.com/2018/05/09/8-bit-game-uses-our-favourite-ic-and-zero-lines-of-code/>

如果一个黑客今天想要构建一个简单的游戏，他或她可以使用 Arduino 板和其他一些零碎东西在大约一个小时内完成，只会得到“黑客在哪里？”但是当你看[OiD]的 [SPEBEG(单人八位电子游戏)](https://figuramania.blogspot.in/2018/05/spebeg-single-player-eight-bit.html)时，你就会明白为什么用老 skool 70s 年代的技术建造任何东西都是如此令人敬畏和教育。

SPEBEG 是一个简单的 8 位游戏，你用操纵杆瞄准目标并开火以获得分数。随着你的分数增加，游戏速度也增加。它不需要一行代码，因为整个设计完全基于硬件。它使用古老的 555。显示屏是一个 8×8 的 LED 矩阵，同时分数和级别显示在两个 7 段 LED 显示屏上。

一条 8 位总线构成了游戏的主干，它由许多 74 系列 TTL 逻辑连接在一起。555 提供了一个 47 kHz 的辅助时钟，而整流二极管后的 100 Hz 信号用于引入每个游戏所需的基本“随机性”。[OiD]很好地描述了整个电路，它将电路分解成字节大小的块，并逐一介绍。使用现代技术构建如此简单的东西，他需要超过 25 种不同的芯片来构建，最终花费了近 200 €。

但是这个项目还有一个让我们惊讶的地方，那就是它的建造技术。[OiD]购买带有超长引脚和许多细漆包线(绝缘)的 IC 插座。一个带有精细尖端和高温设置的焊接站允许他加热铜线的末端以熔化其珐琅绝缘，这样它就可以被焊接到长插脚插座上。通过这种方法，他使用点对点焊接组装电路，非常像[绕线](https://hackaday.com/2018/05/04/ask-hackaday-whatever-happened-to-wire-wrapping/)。只是，他没有把电线包起来，而是焊接起来。

尽管他尽了最大努力，但当他五年前第一次制作这款游戏时，它几乎是不可玩的。他最近把它从仓库里拿出来，消灭了所有的硬件错误，并很好地修复了它。休息之后请看视频。[OiD]的项目显然比这个游戏简单得多，这个游戏是根据最初的街机 Pong 示意图制作的。

 [https://www.youtube.com/embed/qwYVKi0-5X4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/qwYVKi0-5X4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

