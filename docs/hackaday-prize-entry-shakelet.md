# Hackaday 奖参赛作品:Shakelet

> 原文：<https://hackaday.com/2016/07/07/hackaday-prize-entry-shakelet/>

失聪的人听不到声音，但这并不意味着他们感觉不到振动。为了他的 Hackaday 奖参赛作品，[Alex Hunt]正在开发 [Shakelet，这是一种振动腕带，用于通知听障人士](https://hackaday.io/project/10531-shakelet-alerts-for-the-hard-of-hearing)电话、门铃和其他声音警报。

为了解决区分不同来源的不同声音的困难，[Alex 的]希望将小型声音传感器直接连接到声音发射设备上。传感器与腕带进行无线通信。如果腕带接收到来自其中一个传感器的触发信号，它就会通过振动提醒佩戴者。它还通过以某种颜色闪烁 RGB LED 来显示哪个设备触发了警报。他的想法的第一个试验板原型证实了这个概念的可行性。

在解决了传感器灵敏度的几个小问题后，[Alex]现在有了一个工作原型。这种腕带有一个寻呼机电机，由 ATMEGA168 控制。两个 NRF24L01+ 2.4 GHz 无线收发器模块负责通信。声音传感器运行在较小的 ATTiny85 上，使用压电盘作为麦克风。看看下面的视频，Alex 展示了他的身材:

 [https://www.youtube.com/embed/0J-7ZLrl1eY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/0J-7ZLrl1eY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2016](http://hackaday.io/prize) is Sponsored by: [![Atmel](img/2e52aec37df7a9bb2e83735e78e154fe.png)](http://hackaday.io/atmel)  [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](http://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](http://www.digikey.com/)  [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](http://supplyframe.com/)