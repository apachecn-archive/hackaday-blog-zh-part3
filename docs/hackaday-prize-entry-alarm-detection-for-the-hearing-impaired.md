# Hackaday 奖参赛作品:听力受损者的警报检测

> 原文：<https://hackaday.com/2016/09/12/hackaday-prize-entry-alarm-detection-for-the-hearing-impaired/>

几年前，[K.C. Lee]半夜醒来闻到烟味。他正在加热器旁烘干一个蒲团，蒲团着火了。烟雾探测器在这种情况下会有所帮助，但对于听力受损的人来说不会有帮助。因为我们在 Hackaday 奖的辅助技术部分，[KC]决定在他之前的工作基础上建立一个闹钟——一个当闹钟响起时会告诉任何人的设备

烟雾探测器和其他报警器出奇地标准化——声音很大，大约 3kHz。(并非巧合地在 3/4”压电盘的共振频率附近。)一些现代闹钟使用 520 Hz 的闹钟，但在任何一种情况下，当查看音频频谱时，您看到的都是非常大的声音和非常窄的峰值。

[KC]的警报探测器依靠这一特性来探测警报，并点亮、振动或真正做任何其他可以电子控制的事情。目前，该设备是一个基于 STM32F0 的微型设备，带有一个旧的诺基亚 LCD 作为频谱分析仪，每当检测到警报时，整个设备都会点亮。这很简单，也很有效，是 Hackaday 奖辅助技术部分的一个很好的参赛作品。

The [HackadayPrize2016](https://hackaday.io/prize) is Sponsored by:[![Atmel](img/2e52aec37df7a9bb2e83735e78e154fe.png)](https://hackaday.io/atmel) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://www.digikey.com/) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/)