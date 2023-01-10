# Hackaday 奖参赛作品:开放式窄带 RF 收发器

> 原文：<https://hackaday.com/2017/07/14/hackaday-prize-entry-open-narrowband-rf-transceiver/>

当我们希望为我们的设备添加无线控制时，我们有如此多的选择，因为技术已经为我们的实验提供了一系列廉价的设备和分线板。几美元就能满足你所有的无线需求，无论你选择什么频率或协议。然而，这种无限的可用性有一个问题，它们通常相当不透明，只给用户留下他们的板载固件选择呈现的内容。

来自[Samuelák]的[开放式窄带 RF 收发器](https://hackaday.io/project/18032-open-narrowband-rf-transceiver)承诺为实验者提供更有用的东西:一个用于 868 或 915MHz 分配的 RF 收发器，可以完全控制所有传输参数。可以调整频率、带宽和偏差等传输特性，还可以完全控制调制和编码方案。传统模块可能只提供开关键控或频移键控，而该模块可以被编程以提供其芯片组能够提供的任何调制方案。扩频？没问题！

在船上，该设备使用 TI [CC1120](http://www.ti.com/product/CC1120) 收发器芯片，与 [CC1190](http://www.ti.com/product/CC1190) 前端和范围扩展器配对。监管这一切的是一个 ST 微电子 [STM32F051](http://www.st.com/en/microcontrollers/stm32f0x1.html) 微控制器，正如你所料，程序员完全可以访问它。接口可以是 USB，通过 FTDI 串行芯片，或者直接通过串行端口。

市场上有大量的收发器芯片等待开发，所以看到这样的电路板真的很好。值得注意的是，CC1120 的频带比 CC1190 宽得多，并且具有不同的前端和 PA 电路，这可以覆盖其他分配，包括一些业余波段。

The [HackadayPrize2017](https://hackaday.io/prize) is Sponsored by:[![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Texas Instruments](img/3734f1c96ffff85ea2a7eaddc92844ba.png)](https://hackaday.io/ti)