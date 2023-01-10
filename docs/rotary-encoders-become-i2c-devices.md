# 旋转编码器成为 I2C 设备

> 原文：<https://hackaday.com/2018/04/15/rotary-encoders-become-i2c-devices/>

旋转编码器是蜜蜂的膝盖。您不仅可以获得绝对定位，还可以使用旋转编码器(下面有一个别致的 tact 按钮)为任何电子项目提供简单的用户界面。不过，旋转编码器有一个问题:它将使用格雷码或一些奇怪的东西，让旋转编码器与您的代码一起工作并不像一个简单的按钮那么容易。

对于他的 Hackaday Prize 项目，[fattore.saimon]提出了在任何项目中使用多个旋转编码器的解决方案。[这是一块将旋转编码器变成 I2C 装置的板](https://hackaday.io/project/122039-i2c-encoder-v2)。现在，不再需要计算上升沿和下降沿，向项目添加旋转编码器就像连接四根电线一样简单。

该项目是围绕 PIC16F18344 构建的，pic 16 f 18344 是一种小型但功能惊人的微控制器，它可以读取旋转编码器并作为 I2C 从设备输出数据。板上还有几个用于 RGB LED 的引脚，通用引脚，能够设置 I2C 地址的所有 7 位(谁想要 127 个旋转编码器？)，以及用于将几块板连接在一起的堞形孔。

这个项目是[fattore]早期的 [I2C 编码器](https://hackaday.io/project/27611-i2c-encoder)的更新，当前版本有很多改进。它略小，有更好的连接器，并使用更强大的微控制器。这正是你所需要的，如果你想要一吨的旋转编码器，所有这些酷的互动项目。

The [HackadayPrize2018](https://hackaday.io/prize) is Sponsored by: [![Microchip](img/20eb9d92b47da4c15177567c02a65727.png)](https://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey)  [![Supplyframe](img/2d012d9fc9c7873688699aeadb4742d2.png)](https://supplyframe.com/)