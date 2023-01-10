# 破解 Capcom 的 CPS2 安全案例

> 原文：<https://hackaday.com/2018/06/06/cracking-the-case-of-capcoms-cps2-security/>

我们喜欢深入钻研某项专业技术，越晦涩越好。你正在窥视一个世界，按理说，你根本不知道它的存在。少数几个人开发了这个系统，据他们所知，没有人会过来分析和研究它，以了解它是如何一起运行的。但是他们没有预料到一个有时间的好奇黑客的坚韧。

[爱德华多·克鲁兹]在记录这样一个系统方面做得非常出色，这个系统就是 Capcom CPS2 街机版中的反盗版机制。他最近写信告诉我们，他已经在系统上发布了他的第三篇也是最后一篇文章，这一次重点是[弄清楚 CPS2 板上一个神秘的六引脚接头做了什么](http://arcadehacker.blogspot.com/2018/05/a-journey-into-capcoms-cps2-silicon-part3.html)。从其他人那里听到摆弄这个头球偶尔会导致 CPS2 板自动删除游戏，他知道这一定是什么重要的事情。 *Hackaday Protip:* 如果它附有自毁机制，那可能是最酷的部分。

[![](img/397df822460e8682401aae23e05e714b.png)](https://hackaday.com/wp-content/uploads/2018/06/cps2_detail.png) 他顺着由头连接器传来的痕迹，在丝印上鉴定为 C9，回到一个标有 DL-1827 的定制卡普空 IC。在打开 DL-1827 的盖子并把它放在显微镜下之后，[Eduardo]有了一个非常惊人的发现:它实际上对来自头部的信号没有任何作用。一旦芯片加电，它只是充当这些信号的通道，这些信号被重定向到另一个芯片:DL-1525。

[Eduardo]指出，这种故意混淆哪些芯片实际上连接到电路板上的不同接头的做法是 Capcom 等公司用来增加侵入其电路板难度的经典伎俩。一旦他发现 DL-1525 才是他真正想要的，他就能够利用从他早期作品中收集到的[信息来拼凑这个谜题。](http://arcadehacker.blogspot.com/2018/01/a-journey-into-capcoms-cps2-silicon.html)

这个特殊的 [CPS2 黑客之旅从去年 3 月](https://hackaday.com/2016/09/15/desuiciding-capcom-arcade-boards/)才开始，但是【Eduardo】从 2014 年开始就已经在[调查街机游戏板上的版权保护系统了。](https://hackaday.com/2014/12/12/reverse-engineering-capcoms-crypto-cpu/)

【感谢 Arduino Enigma 的提示。]