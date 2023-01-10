# Hackaday 奖参赛作品:编程杂耍道具

> 原文：<https://hackaday.com/2016/06/07/hackaday-prize-entry-programming-juggling-props/>

学习如何变戏法需要胆量，但是一旦你学会了，你很快就会转向环、链锯和那些非常奇怪的杂耍俱乐部。作为 Hackaday 奖的参赛作品，[Laurent B]和[michael.creusy] [将物联网引入杂耍俱乐部](https://hackaday.io/project/10764-rastello-club)。他们的 Rastello Club 是一个发光的 LED 照明杂耍道具，带有 9 自由度 IMU，使杂耍看起来更酷。

因为任何东西都有市场，所以发光的、可编程的杂耍俱乐部已经存在。不过，这些俱乐部有一些限制。他们没有九轴方向传感器，没有与计算机或各个俱乐部之间的通信，当然他们不是开源的。拉斯泰罗俱乐部解决了这些问题，使可编程杂耍俱乐部易于使用，并增加了一堆可视化。

当然，在这些杂耍俱乐部里面有一束 led，以及一个相当强大的 STM32F4 ARM 处理器、9 轴 IMU 和电池充电电路。各个俱乐部和计算机之间的无线电连接将通过 RFM75 收发器进行处理。不，不是 WiFi，不是蓝牙，不是 ZigBee 这种无线电模块比蓝牙更快，比 Zigbee 更便宜，比 ESP8266 更省电。

The [HackadayPrize2016](http://hackaday.io/prize) is Sponsored by: [![Atmel](img/2e52aec37df7a9bb2e83735e78e154fe.png)](http://hackaday.io/atmel)  [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](http://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](http://www.digikey.com/)  [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](http://supplyframe.com/)