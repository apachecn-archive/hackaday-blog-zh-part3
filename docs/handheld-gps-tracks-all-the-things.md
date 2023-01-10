# 手持 GPS 追踪所有的东西

> 原文：<https://hackaday.com/2018/02/19/handheld-gps-tracks-all-the-things/>

由于每部智能手机上都有 GPS，人们忘记手持 GPS 设备仍然存在是情有可原的。[_Traveler]为了在即将到来的几次旅行中保持准确的数据，进行了定制，这导致了这个 [GPS 数据记录器](https://imgur.com/a/ifCec)。

对[_Traveler]进行监控的是 Ublox M8N GPS，它是全时工作的，每 30 秒记录一次数据，最多可持续 2.5 天。所有数据都保存在 SD 卡中，ESP32 充当大脑，通过 WiFi 更容易下载信息。在跟踪明显的数据(如位置、速度和时间)的同时，这款数据记录器还可以在 ePaper 屏幕上显示温度、海拔、黎明和黄昏，这是节省电池的绝佳选择。

这一次的原型制作过程非常简单。第一个完整的构建使用原型板上的点对点焊接将几个分支模块连接在一起。之后，PCB 设计包含相同的模块，具有用于 ESP 齿形边缘的占位面积和用于 USB 充电板、SD 卡板、ePaper 等的头部占位面积。所有这些都在 3D 打印外壳中找到了希望。在 Arduino IDE 中编码了相当多的时间之后，记录器已经为[_Traveler]的下一次旅行做好了准备！

至于现场的功耗，[_Traveler]表示，GPS 需要一些时间来获得一个正确的位置 ESP 一直在考虑电池寿命——并计划在更短的时间内进行调整。

并非所有的 GPS 追踪器都是一样的:有时你所需要的只是一个为你的慢跑准备的简易追踪器，或者知道你的路线上每个坑洞的确切位置。

[通过[/r/电子](https://www.reddit.com/r/electronics/comments/7wx9zo/3_months_later_finally_finished_the_gps_logger_i/)