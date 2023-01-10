# 通过 DMA 实现更好的 led

> 原文：<https://hackaday.com/2017/06/19/better-leds-through-dma/>

虽然普通黑客读者已经知道如何用微控制器使 LED 闪烁，并转向稍微更具挑战性的项目，如在 6502 汇编中求解纳维尔-斯托克斯方程，但这并不意味着没有新手的空间。[Rik]发表了一篇很棒的教程，讲述了为了更炫的东西而滥用 DMA。为什么会有人想学习 DMA 技术？当然是为了闪闪发光的东西。

本教程假设了解 LED 多路复用和 LED 矩阵，或者基本上是 XY 网格上连接在一起的一束 LED。驱动 8×8 led 网格的简单方法是将 8 个阴极连接到微控制器的 GPIO 引脚，将 8 个阳极连接到另一组 GPIO 引脚，并根据需要提供和吸收电流。利用移位寄存器可以减少引脚数，利用 PWM 可以实现 LED 调光。我们为期八周的 Arduino 强化课程到此结束。

由于微控制器没有陷入 20 世纪 80 年代的困境，新技术可以用来驱动这些 LED 矩阵。大多数更强大的 ARM 微控制器都带有 DMA，这是一种用于直接内存访问的外设。DMA 控制器可以简单地在内存和引脚之间来回移动位，而不是让 CPU 做所有的工作。这意味着闪光灯项目和发光二极管。

[Rik]对 LED 进行 DMA 的方法包括在代码中设置一个大的 ol 数组，正确初始化 DMA 外设，并将 LED 矩阵连接到几个引脚。这项技术可以扩展到 64 级亮度的动画，如果没有 DMA 控制器，这将需要惊人的处理能力(至少对于微控制器来说)。

这些实验中使用的设置是 STM32F103 Nucleo 板和 OpenSTM32 IDE。[Rik]已经在 GitHub 上发布了所有的代码[，当然，我们也鼓励你尝试一下。](https://github.com/riktw/DriveLedsWithDMA)