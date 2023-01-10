# 更小更便宜的 Arduino

> 原文：<https://hackaday.com/2017/02/21/smaller-cheaper-arduino/>

嗯，老实说，[迈克尔·迈耶]的 STM8 Arduino(称为 [Sduino](https://github.com/tenbaht/sduino/blob/master/docs/index.md) )实际上与 Arduino 没有太大关系，除了精神上。STM8 是一款 8 位处理器。它非常便宜，而且有一些方便的特殊电机控制功能。有一个重要的图书馆可供使用。然而，使用库和建立构建可能是一件痛苦的事情。

就像 Arduino IDE 如何为 gcc 提供库和构建系统一样，Sduino 为 sdcc 编译器提供类似的库和构建系统，sdcc 编译器可以针对 STM8。然而，如果你期待的是 Arduino 的 GUI 或者一个 Arduino 库的完整仿制品，你不会得到它。

也就是说，你可以得到很多兼容的库。命令行 Makefile 易于设置和使用。为什么不用“普通”的 Arduino 呢？STM8 不仅价格低廉，而且可以利用专门的硬件进行正交解码等操作。此外，低功耗模式也非常低。

不要让 Makefile 影响你。标准的闪烁草图看起来和 Arduino 版本一样。下面是所需的 Makefile:

```
BOARD_TAG = stm8sblue
include ../../sduino/sduino.mk
```

就是这样。不要太用力。

它支持一个便宜的简单分线板，以及本文顶部的 ESP-14，该板带有一个 ESP8266 和一个 STM8 控制器。花大约 3 美元，你就可以得到一个 STM8003 CPU 和 WiFi 功能。很难打破这个记录。[埃利奥特·威廉姆斯]刚刚试了试那块板，发现 [ESP-14 很“怪异”](https://hackaday.com/2017/02/13/hacking-on-the-weirdest-esp-module/)。他可能是对的，但这给了你一个简单的使用方法。

对发现板的 [STM8 版本的支持应该即将推出。](https://hackaday.com/2009/11/23/stm8s-discovery-microcontrollers-reach-a-new-low/)