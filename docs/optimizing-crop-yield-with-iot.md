# 利用物联网优化作物产量

> 原文：<https://hackaday.com/2015/11/16/optimizing-crop-yield-with-iot/>

对于最近的一次黑客马拉松，一群陌生人(现在是朋友！)创建了[作物方格](https://github.com/fauria/crop-squares/blob/master/README.md)——一个旨在通过更好地跟踪天气和土壤条件来优化作物产量的系统。

该活动在马德里举办，名为[未来黑客物联网版](http://futurehacks.co/)，目标是构建颠覆性的物联网解决方案，帮助改变世界。在 54 小时内。

作物方格背后的概念是用 Dizmo 制作一个图形用户界面，清楚地显示你的作物在网格系统中的状态。对于原型，他们在盆栽植物中使用了一个带有湿度传感器的 Arduino Pro Mini 来检测湿度水平，而树莓 Pi 也收集了正在观察的区域的天气数据。Arduino 使用 ESP8266 WiFi 模块远程传输数据。为了展示该系统如何在自动化意义上使用，他们连接了另一个 Arduino(这次是 Leonardo ),一旦水分水平下降到某个阈值以下，就倒水。

Crop Squares 赢得了最佳推介奖以及 Dizmo 的最佳整合奖——干得好，伙计们！

说到湿度传感器——你知道你可以用一些熟石膏和钉子来制作自己的传感器吗？