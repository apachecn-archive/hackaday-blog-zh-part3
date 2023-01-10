# 一种通用 USB 转正交编码器

> 原文：<https://hackaday.com/2017/06/12/a-universal-usb-to-quadrature-encoder/>

电脑鼠标早在 Mac 出现之前就存在了，大多数老式 8 位电脑都有一些可以使用鼠标的软件。这些老鼠有球和正交编码器。虽然存在将这些旧鼠标转换成 USB 设备的转换器，但反其道而行之并不常见。[西蒙]以小老鼠的形式找到了这个问题的答案。它将 USB 鼠标变成了可以与 BBC Micro、Acorn Master、Acorn Archimedes、Amiga、Atari ST 等一起使用的东西。

SmallyMouse2 的设计使用 AT90USB 微控制器，支持 USB 设备和主机模式，并允许一些 GPIOs。该微控制器有效地将 USB 鼠标转换为 BBC 微型用户端口 AMX 鼠标、通用正交鼠标和 10 针扩展接头。固件使用 [LUFA USB](http://www.fourwalledcubicle.com/LUFA.php) 堆栈，这是这些怪异的 USB 改造计算机项目的常见选择。

该项目是完全开源的，从 KiCad 项目复制到固件的所有文件都可以在【Simon】的 GitHub 上获得[。如果你的阁楼里有一台这种经典的复古电脑，也许是时候检查一下你的鼠标是否还在。如果没有，这是一个完美的项目，深入研究过去的经典图形用户界面。](http://www.waitingforfriday.com/?p=827)