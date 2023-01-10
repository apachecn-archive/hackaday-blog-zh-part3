# Hackaday 奖参赛作品:嗅探除颤器数据

> 原文：<https://hackaday.com/2016/05/22/hackaday-prize-entry-sniffing-defibrillator-data/>

有很多植入式医疗技术实际上是一个黑匣子。胰岛素泵监测血糖并输送胰岛素，但你不能准确地插入 USB 电缆并下载数据。起搏器和心脏除颤器也是如此。对于这些患者，数据通常被传输到基站，然后通过互联网发送，以帮助医生做出决定。病人永远看不到这些数据，但是通过一些工作和软件定义的无线电，[hack aday . io 上的一个团队正在破解代码](https://hackaday.io/project/11323-iceedata)来监听这些植入的医疗设备。

ICeeData 背后的团队是在去年 4 月拉脱维亚举行的一次健康科技黑客马拉松上组建的。一名团队成员植入了除颤器以保持其心脏的形状，并携带了植入的基站。该植入物通过 402-405MHz 无线电进行通信，这是一个廉价的 RTL-SDR 电视调谐器加密狗可以轻松访问的频谱区域。

现在的计划是拦截植入物和基站之间的通信，解码数据包，破译协议，并理解数据的含义。这是一个经典的逆向工程任务，对任何无线电协议都是一样的，只是这个协议的传输来自人体内部。

The [HackadayPrize2016](http://hackaday.io/prize) is Sponsored by: [![Atmel](img/2e52aec37df7a9bb2e83735e78e154fe.png)](http://hackaday.io/atmel)  [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](http://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](http://www.digikey.com/)  [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](http://supplyframe.com/)