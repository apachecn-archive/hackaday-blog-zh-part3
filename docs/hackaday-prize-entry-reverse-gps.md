# Hackaday 奖品入口:反向 GPS

> 原文：<https://hackaday.com/2016/06/22/hackaday-prize-entry-reverse-gps/>

每次你观看 SpaceX 直播，看到一个巨大的成功或驳船上的火球(选择你的毒药)，你可能会看到几个立方体上升。每当你看到联盟号发射时，它莫名其妙地先在 liveleak.com 发射，你就会看到几个立方卫星上升。现在有数百颗 10 厘米的卫星在轨道上运行，两年前 Hackaday 奖的获得者 SatNogs 为所有这些立方体卫星提供了一个全球地面站网络。

全球卫星跟踪地面站网络有一个重大问题:你需要知道所有这些立方体卫星的轨道。这是一个问题，因为所有的低地球轨道部署都没有推进器，也很少有姿态控制。这些立方体卫星在稀薄的大气中翻滚，导致几个月内无法预测的轨道。

[hornig]正致力于解决跟踪数百颗卫星的问题，也就是简单地说，反向 GPS。该系统不是使用多个卫星来确定地球上的位置，而是使用地球表面的多个接收站来确定卫星的轨道。

[hornig]分布式地面站网络的硬件如你所料的那样简单。它只是一个 RTL-SDR 电视调谐器 USB 加密狗，几根天线，一个 GPS 接收器和一个连接到互联网的树莓 Pi。这个装置需要简单；与 SatNogs 不同，在偏远地区的单个基站仍然可以接收来自 cubesats 的数据，该系统需要多个接收器，所有接收器都在卫星的视野范围内。

现代 GPS 卫星系统是有史以来最伟大的技术成就之一。美国不仅需要将高度精确的时钟送入轨道，系统的设计者也需要考虑相对论效应。反向操作 GPS 确定地面卫星的轨道——同样是一个令人印象深刻的项目，也是今年 Hackaday 奖的有力竞争者。

The [HackadayPrize2016](http://hackaday.io/prize) is Sponsored by: [![Atmel](img/2e52aec37df7a9bb2e83735e78e154fe.png)](http://hackaday.io/atmel)  [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](http://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](http://www.digikey.com/)  [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](http://supplyframe.com/)