# Hackaday 奖参赛作品:房间里有一头大象

> 原文：<https://hackaday.com/2016/06/06/hackaday-prize-entry-theres-an-elephant-in-the-room/>

大象和人类并不像你希望的那样相处融洽。人象冲突导致了厚皮动物和人类的死亡。大象袭击庄稼。大象被火车撞死。显然，大象在哪里是有用的知识。这是[Neil]为参加 Hackaday 奖正在解决的问题。他的项目探测大象，不管它们是在铁路上，在狼吞虎咽地吃庄稼的田野里，还是……在房间里。

[Neil]的目标很简单——他正在建立一个分布式大象检测系统，可以部署在铁路交叉路口、森林和农田之间，以及沿着已建立的大象足迹。这给[尼尔]提出了两个问题:探测大象，并把信息传达给人类。

为了检测大象，[Neil]依靠网络摄像头和运行 OpenCV 视觉处理的 Raspberry Pi 3。他要么比较直方图，以实现更快、资源更少的图像处理，要么进行特征匹配。每个探测器都配备了一个 PIR 传感器，所以至少 Pi 不会一直在寻找大象。

通知人类大象的存在是该项目的下一步，这可能比首先找到大象还要困难。[Neil]决定在每个 Pi 上使用 ZigBees 与至少一个基站通话。然后，这个基站通过更长距离的无线电链路向当地居民发送消息。在非洲稀树草原的中部将一群私人信息网络连接起来是一个困难的问题，但是通过将这个项目的通信方面分成两个无线电链路，[Neil]有了一个相当健壮的解决方案。

The [HackadayPrize2016](http://hackaday.io/prize) is Sponsored by: [![Atmel](img/2e52aec37df7a9bb2e83735e78e154fe.png)](http://hackaday.io/atmel)  [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](http://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](http://www.digikey.com/)  [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](http://supplyframe.com/)