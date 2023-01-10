# 用 Pi 零点控制 RGB LEDs

> 原文：<https://hackaday.com/2016/02/14/controlling-rgb-leds-with-the-pi-zero/>

Pi Zero 是一个很棒的硬件，即使你没有为它设计另一个 USB 集线器。[Marcel]想要从他的手机中控制几个 RGB LED 灯条，虽然有很多奇特的方法可以做到这一点，但真正需要的是一个 Pi 零和几个可能已经在你的零件抽屉里敲打的零件。

这不是一个控制单个可寻址 RGB LEDs(如 NeoPixels、WS2812s 或 APA102 LEDs)的项目。这只是一个用~~五个~~四个连接器控制 RGB LEDs 的项目:红、绿、蓝、电源、~~和~~或地。这些是你能得到的最简单的 RGB LEDs，有时它们足够好，足够便宜，是项目中多色闪光灯的完美解决方案。

因为这些 RGB LEDs 很简单，这意味着控制它们非常容易。[Marcel]只是将一个晶体管连接到 Pi 上的三个 PWM 引脚，并使用 TIP122 晶体管来驱动红色、绿色和蓝色 led。你一定会[爱上这些齿尖包部件](http://hackaday.com/2015/08/17/you-can-have-my-tips-when-you-pry-them-from-my-cold-dead-hands/)！

led 的控制是通过 [lighttpd](http://www.penguintutor.com/linux/light-webserver) 完成的。这确实意味着需要一个 USB WiFi 加密狗来控制互联网上的 led，但这是迄今为止我们见过的最简单的方式来添加多色 blinkies 到网络上。

* * *

![Raspberry_Pi_LogoSmall](img/87d7e34f7ac8cc3ae6c8619ad96c149e.png)

树莓派零竞赛由 Hackaday 和 Adafruit 主办。奖品包括 Adafruit 的树莓派零和 Hackaday 商店的礼品卡！
[查看所有参赛作品](https://hackaday.io/submissions/adafruitpizerocontest/list) || [现在就进入你的项目吧！](https://hackaday.io/contest/9326-adafruit-pi-zero-contest)