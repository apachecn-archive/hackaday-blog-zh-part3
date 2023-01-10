# 1Wamp，开放式硬件吉他放大器

> 原文：<https://hackaday.com/2015/11/30/1wamp-an-open-hardware-guitar-amplifier/>

[electro mash]的人最近发布了[1 wamp——一个 1 瓦的开放式硬件吉他放大器](http://www.electrosmash.com/1wamp),功能齐全。它包括一个基于 JFET 的前置放大器，一个[大 Muff Pi](https://en.wikipedia.org/wiki/Big_Muff) 又名基于 BMP 的音调控制和一个 LM386 功率放大器。双 JFET 前置放大器提供了类似电子管的声音，BMP 提供了良好的音调范围，而 LM386 可以驱动从耳机到音箱的各种类型的输出。

1Wamp 具有音调、音量和增益控制、扬声器/音箱输出、带集成衰减器开关的耳机输出和 aux。输入。辅助。输入很方便，因为它将任何线路电平输入信号添加到吉他声音中，允许您使用节拍器或 MP3 背景音乐或鼓基础来练习。它既可以用 9V 电池供电，也可以通过外部电源供电。【ElectroSmash】已经发布了所有原生 [KiCad 设计文件](http://www.electrosmash.com/forum/1wamp/92-1wamp-schematic-layout-open-hardware-files?lang=en)。如果你想快速浏览一下设计，可以查看一下[的 PDF 示意图](http://www.electrosmash.cimg/tech/1wamp/vault/1Wamp-schematic.pdf)和[的材料清单](http://www.electrosmash.cimg/tech/1wamp/vault/1Wamp-bill-of-materials.pdf)。还有一个方便的[组装手册](http://www.electrosmash.cimg/tech/1wamp/vault/How-to-Build-1Wamp.pdf) [PDF]，展示了如何通过五个简单的步骤来构建它。

他们的博客文章对设计的每个部分提供了极其详细的电路分析，从消除电源“嗡嗡声”的电源滤波器，一直到降低噪声的 PCB 布局考虑。示波器屏幕截图提供信号分析，显示整个电路中的偏置点和信号电平。解释了每个组件的值的选择，以及更改这些值的后果。这使得根据个人喜好定制 1Wamp 变得非常容易。我们还注意到推荐和替代 JFET 晶体管的 SPICE 模型，以防您需要通过更改元件值来定制设计。

在他们的帖子中还有很多音频放大器的琐事、参考和链接。这包括对 LM386 运算放大器的详细分析。想给你的 1Wamp 增加一些光彩吗？有很多关于[如何给安装在标准金属外壳中的放大器添加酷炫 LED 照明](http://www.electrosmash.com/forum/1wamp/85-using-the-plexiglas-cover-as-a-lighting-plate?lang=en)的便利提示。然而，PCB 有一些非常好的图形，所以丙烯酸夹层式外壳看起来最好。观看视频，了解 1Wamp 的特性并展示其性能。说到音频电子产品，这是他们早期的项目之一——[一个开源的 Arduino 吉他踏板](http://hackaday.com/2013/12/21/an-opensource-arduino-guitar-pedal/)。

这一水平的文档证明了几件事，最明显的是对这一设计的热爱和对那些将使用和修改这一放大器的人的深刻考虑。对于你自己的开源设计来说，这是一个很好的模式。

 [https://www.youtube.com/embed/cFPIS3gorQA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/cFPIS3gorQA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

