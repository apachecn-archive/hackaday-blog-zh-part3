# 三瓦可单独寻址的 RGB LEDs

> 原文：<https://hackaday.com/2015/11/06/three-watt-individually-addressable-rgb-leds/>

虽然彩色 blinky 项目的黄金标准是单独可控的 RGB LEDs，但通常的产品并不真正令人印象深刻。是的，几百个新像素，WS2812 或其他 RGB LEDs 会灼伤你的视网膜，但如果你想要的是如此夸张的闪亮东西，以至于冒犯了你所信仰的任何创造者，那该怎么办？

[就是它了](http://ytai-mer.blogspot.com/2015/11/pixie-bright-things-come-in-small.html)。[Ytai Ben-Tsvi]创造了一种可单独寻址的 RGB LED，称为 Pixie，非常适合您需要明亮、多彩的东西，并希望在此过程中蒙蔽一些人的时候。

WS2812s 和 Neopixels 基本上是 RGB LEDs，内部隐藏着一个小型微控制器，到目前为止，中国还没有一家设计室或晶圆厂疯狂到在已经功率过大的 LED 上添加一个这样的小芯片。为了构建 Pixie，[Ytai]采用了一个裸露的 RGB LED 模块，并添加了一个微控制器——在本例中是 PIC12FF157X。它并不是一个功能强大的微控制器，但它可以处理可单独寻址的 RGB 的类似移位寄存器的功能，并增加了伽马校正、过热保护(当你将这么多功率注入一个小电路板时，这是必要的)，以及每个单独 LED 的其他保护措施。

[Ytai]正在与 ada fruit 合作生产这些小精灵，尽管它们相当昂贵，每个 LED 15 美元，但你不需要太多就能失明。