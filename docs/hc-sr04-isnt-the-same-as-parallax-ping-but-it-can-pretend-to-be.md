# HC-SR04 和视差 PING 不一样))但是可以装！

> 原文：<https://hackaday.com/2015/09/22/hc-sr04-isnt-the-same-as-parallax-ping-but-it-can-pretend-to-be/>

***“只是软件！”*** 一句让嵌入式系统软件开发人员心惊胆战的话。当软件人员在硬件中发现一个 bug，而其他人认为在软件中修复这个 bug 比修改新的硬件版本更容易时，人们经常会说这句话。难怪软件总是迟到。

和我们大多数人一样，[Clint Stevenson]是他自己的硬件和软件专家。他想在原型中使用较便宜的 HC-SR04 超声波测距仪。从长远来看，他希望能够选择 Parallax PING 或 MaxBotix 超声波传感器，以便在户外获得更好的性能。他对 SR04 的硬件[破解使这成为一个软件问题](http://www.cascologix.com/blog/hc-sr04-ping-sensor-hardware-mod)，他也设法解决了这个问题！

[Clint]正在使用基于 Parallax PING 的 Arduino 库，该库使用一个引脚来触发和回应。HC-SR04 使用单独的引脚。最初，他修改了 Arduino 库以接受双引脚方法。但考虑到他的长期目标，他还修改了 HC-SR04 传感器，去掉了板上上拉电阻，并在连接器端增加了一个新的电阻来合并信号。这给了他一个 SR04，它可以与基于单引脚的库一起工作。

我们已经看到了用于[感测水深](http://hackaday.com/2013/04/30/sump-pump-alarm-sends-text-message-as-water-rises/)和[产生音乐](http://hackaday.com/2011/02/13/range-finder-musical-toy/)的 Parallax PING 项目。使用[Clint 的]技术，这些可以被破解以使用 HC-SR04。

[Arduino 和 HC-SR04 照片来自 [Blax 实验室](http://www.blaxlab.com/2015/06/connecting-and-programming-hc-sr04.html)