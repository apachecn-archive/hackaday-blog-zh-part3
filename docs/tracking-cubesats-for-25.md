# 追踪立方体卫星，25 美元

> 原文：<https://hackaday.com/2018/06/01/tracking-cubesats-for-25/>

立方体卫星是微小的卫星，在发射过程中作为次要有效载荷跟随。它们的重量必须低于 1.33 千克，而且通常造价低廉。甚至还有针对这些小飞船的开源设计。在过去几年里，已经发射了 800 多颗立方体卫星，计划在不久的将来发射更多的卫星。

[Thomas Cholakov]将自制的苜蓿叶形天线耦合到软件定义的无线电，以跟踪其中一些卫星。该天线由切割成正确长度的铜包线制成，可接收 437 MHz 信号。四个环路连接在一起，端接至一个 RF 连接器。

这个自制天线连接到一个 [RTL-SDR](https://hackaday.com/tag/rtl-sdr/) 加密狗。加密狗接收卫星发送的信标信号，并将数据提供给个人电脑。由于卫星的运动，通过频率的[多普勒频移](https://en.wikipedia.org/wiki/Doppler_effect)可以很容易地识别它们的信标。

[托马斯]使用 [SDR 控制台](http://www.sdr-radio.com/Console)接收来自卫星的数据。虽然演示只显示了基本的接收，更多关于解码这些卫星的信息可以在 [SDR 卫星](http://www.sdr-satellites.com/)网站上找到。

这看起来像一个有趣的周末项目，可能是最便宜的航空航天相关项目。休息之后，观看完整的视频，解释如何建立和设置天线和加密狗。

 [https://www.youtube.com/embed/t5pihYcRWPA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/t5pihYcRWPA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

