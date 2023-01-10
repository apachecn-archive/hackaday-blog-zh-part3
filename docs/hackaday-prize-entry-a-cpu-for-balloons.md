# Hackaday 奖参赛作品:气球的 CPU

> 原文：<https://hackaday.com/2016/08/22/hackaday-prize-entry-a-cpu-for-balloons/>

发射高空气球需要广泛的知识。为了做好这件事，你显然需要了解电子学和编程来获得温度、压力和 GPS 数据。你必须研究哪种相机能拍出好照片，而且容易编程。那里很冷，这意味着你需要一些绝缘材料来保持电池的温度。如果你想找到你的有效载荷，你还需要一个业余无线电执照。

发射高空气球有很多工作要做，为了他的 Hackaday 奖参赛作品， [[Jeremy]设计了一个简单的嵌入式数据记录器](https://hackaday.io/project/12100-flightcpu)，能够飞行超过 100，000 英尺。

这款气球飞行数据记录器基于非常流行的 ATMega328，包括湿度、温度、压力、加速度计、陀螺仪和磁力计传感器。所有这些数据都记录在 SD 卡上。习惯于批评他们不同意的设计决策的真正工程师可能会嘲笑 7805 稳压器的使用，但在这种情况下，它很有意义。线性调节器浪费的功率不会。它转化为热量，使电池的寿命更长一点。

这个气球数据记录器已经飞行过了，[杰里米]从中获得了一些很棒的照片。这是一个非常多学科项目的一大难题，也是 Hackaday 奖的一大亮点。

The [HackadayPrize2016](https://hackaday.io/prize) is Sponsored by:[![Atmel](img/2e52aec37df7a9bb2e83735e78e154fe.png)](https://hackaday.io/atmel) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://www.digikey.com/) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/)