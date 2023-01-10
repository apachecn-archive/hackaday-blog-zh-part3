# 故障合成器遇到蜂窝 LED 矩阵

> 原文：<https://hackaday.com/2017/03/03/glitchy-synthesizer-meets-honeycomb-led-matrix/>

如果闪烁的灯光或哔哔作响的合成器噪音让你癫痫发作，就不要看[杰森·霍奇基斯]的视频。不过，如果你对通过内置的专用方波合成器以音频驱动的[大型蜂窝状 LED 矩阵](http://hotchk155.blogspot.de/2017/02/meet-wobatron.html)感兴趣，请务必观看。

问题中的 LED 面板被安置在一个时髦的激光切割的蜂窝状挡板中:在我们看来，这是对标准正方形的一个很好的改变。灯是 1/2 瓦(哇！)白色，并且行和列由晶体管驱动器驱动，晶体管驱动器又由移位寄存器控制。我们不完全确定矩阵是如何驱动的，我们希望看到电路图，但它看起来像是某种奇怪的非扫描模式，所有的列和行驱动器同时开启。不管怎样，这是艺术。

它由产生音频方波的逻辑芯片驱动。其中两个信号馈入 LFSR 和 R-2R DAC，然后馈入移位寄存器。输出是混乱的，但是音频和视频似乎相互影响。这是我的一些[最疯狂的逻辑噪音幻想](http://hackaday.com/2015/05/04/logic-noise-taming-the-wild-shift-register/)的视听体现。相当酷。欣赏视频。

 [https://www.youtube.com/embed/N59dmpDMgM8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/N59dmpDMgM8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

