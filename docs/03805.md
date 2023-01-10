# Hackaday 奖参赛作品:戴手套的手会说手语

> 原文：<https://hackaday.com/2016/10/11/hackaday-prize-entry-handson-gloves-speaks-sign-language/>

手套看起来像是 PowerGlove 的替代品，但它比 power glove 好得多。(这并不是说拳王手套不酷。很糟糕。)而且必须如此——它要解决的任务不是玩简单的视频游戏，而是大声读出用户的手语手势，以便不懂手语的人能够理解懂手语的人。

手套需要大量的传感器数据来准确解读用户的手势，Hands|On 也不会让人失望。每个手指上都附着有多个弯曲传感器，这样手套就可以分辨出哪些关节弯曲了。一些手指上有电容触摸板，这样手套可以知道两个手指何时相互接触，这在美国手语字母表中很重要。最后，手套有一个九自由度惯性测量单元(IMU)，因此它可以跟踪俯仰、偏航和滚动以及手的方向。

简而言之，手套接收大量数据。这些数据在 Teensy 3.2 板中被清理和分析，并通过蓝牙发送到最终目的地。在软件方面也做了很多工作(还有一些要做)。如果你对符号分类的支持向量机感兴趣，可以通读一下[项目的报告(PDF)](https://cdn.hackaday.io/files/14915638123360/CapstoneFinalReport.2-22.pdf) 。

手语是大多数聋人的母语，听力群体不能直接理解手语是一种耻辱。打破这一障碍是一个伟大的想法，它是参加 [Hackaday 奖](https://cdn.hackaday.io/files/14915638123360/CapstoneFinalReport.2-22.pdf)的绝佳机会！

The [HackadayPrize2016](https://hackaday.io/prize) is Sponsored by:[![Atmel](img/2e52aec37df7a9bb2e83735e78e154fe.png)](https://hackaday.io/atmel) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://www.digikey.com/) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/)