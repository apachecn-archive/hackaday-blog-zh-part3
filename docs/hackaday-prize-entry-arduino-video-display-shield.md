# Hackaday 奖品入口:Arduino 视频显示盾

> 原文：<https://hackaday.com/2017/10/30/hackaday-prize-entry-arduino-video-display-shield/>

Arduino 是任何微控制器入门的标准。说到显示视频，骨头股票 Arduino Uno 严重缺乏。没有足够的内存来存放帧缓冲区，而且它的速度也不足以进行光束比赛。如果你想从 Arduino 获得视频，它要么很糟糕，要么你需要一些神奇的芯片来实现一切。

[MagicWolfi]的 2017 年 Hackaday 奖参赛作品由一个[视频显示屏蔽](https://hackaday.io/project/21097-arduino-video-display-shield)组成，它非常容易使用，根据项目描述，它可以取代经典的眨眼草图。

该项目以 VLSI VS23S010D-L 芯片为中心，该芯片集成了 1 兆位 SPI SRAM，具有串行和并行接口。集成视频显示器将复合视频信号发送到显示器，模式取决于所需的颜色数量和分辨率:例如，在 640×400 的分辨率下，您可以显示 16 种颜色。正如他所描述的，不是 4K 的视频，但肯定是比武。该芯片预期 3.3 V 逻辑，因此他利用 MC74LVX50 十六进制缓冲器来定制 Arduino 的 5 V，目前他正在开发 shield 的第二版，其中将包括 SPI 闪存。

你可以关注 Hackaday.io 上的项目，或者在[MagicWolfi]的 GitHub 资源库中找到当前的盾设计。

The [HackadayPrize2017](https://hackaday.io/prize) is Sponsored by:[![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Texas Instruments](img/3734f1c96ffff85ea2a7eaddc92844ba.png)](https://hackaday.io/ti)