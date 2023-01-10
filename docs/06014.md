# 能量收集腕表使用多功能光电二极管

> 原文：<https://hackaday.com/2017/05/26/energy-harvesting-wristwatch-uses-a-versatile-photodiode/>

这款能量收集腕表结合了一些有趣的技术。虽然能量收集计时器(被称为[自动手表](http://en.wikipedia.org/wiki/Automatic_watch))已经存在了近 240 年，【bobricius】使用了更容易转移到其他项目的部件和方法。

与早期的机械系统不同，这种设计使用了多功能的 [BPW34 PIN 光电二极管](http://www.vishay.com/docs/81521/bpw34.pdf) (PDF 警告)。 [PIN 光电二极管](http://en.wikipedia.org/wiki/PIN_diode)不同于普通的 PN 二极管，因为有一层未掺杂的“本征”硅将 P 和 N 掺杂层分开。这降低了二极管作为整流器的效用，同时允许更高的量子效率和开关速度。

它们通常用于电信行业，但也有许多有趣的“标签外”应用。例如，BPW34 可以用作固态粒子探测器(虽然对于探测阿尔法粒子，你最好使用 TO-5 封装的东西，如 Hamamatsu S1223-01)。快速的响应速度意味着你可以[用高频激光或环境光发送数据](http://hackaday.com/2015/12/11/hackaday-explains-li-fi-visible-light-communications/)——这是 LED 照明系统或报废 DVD-RW 激光的一个有趣用途。

一些常见的太阳能电池板本质上是大 PIN 光电二极管。这些是你会在太阳能计算器中发现的褐色面板，或者是那些永远挥舞着的金色塑料 neko 神龛之一。它们特别提供出色的弱光性能，这是本项目中使用的能量收集的基础。

非常有趣的是，[能量收集物联网传感器](http://hackaday.com/2017/05/15/hackaday-prize-entry-self-sustained-low-power-nodes/)使用类似的方法在没有电池或市电的情况下工作:非晶硅太阳能电池结合高效超级电容器充电电路。这对于屋顶和工业或农业场所的无线发射机来说非常有用，因为在这些地方市电是不切实际的。此外，由于不需要更换电池，防风雨传感器只需要一个环氧树脂管。

它作为手表的功能好吗？待机时间至少 7 天，观看时间最长 20 分钟，还有一个快速充电的 USB 端口，除非你痴迷地看时间，否则这并不是完全不切实际的。相比之下，自动机械表提供无限的观看时间，但如果没有佩戴一两天，通常会耗尽储存的能量，我们认为 USB 端口是一种比疯狂挥舞手臂更有尊严的给手表上弦的方式。

请观看下面的视频:

 [https://www.youtube.com/embed/MieHTr4xJfM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/MieHTr4xJfM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

