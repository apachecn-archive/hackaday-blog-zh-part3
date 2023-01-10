# 微型 USB 莫尔斯电码信标

> 原文：<https://hackaday.com/2016/02/18/tiny-usb-morse-code-beacon/>

让微控制器发出一些莫尔斯电码相当容易。让帕弗林接手这个项目的有趣之处在于，它驻留在一个带有 ARM 处理器的微型 USB 板上。该板的设计提供适合使用简单方法(如墨粉转移)生产的单面插图。

STM 设备有一个内置的 USB 引导程序。它也可以作为一个串口，这使得项目非常简单。唯一的外部器件是扬声器和光隔离器。该程序通过串行端口提供了一个命令行界面，您可以使用该界面对消息进行编程，并设置其他选项，如速度和消息之间的延迟。该代码可在 [GitHub](https://github.com/s54mtb/stm32projects/tree/master/projects/f0-usb-beacon) 上获得。

你可能会说，信标不应该需要 USB 端口，我们已经看到了符合要求的替代方案。如果你想要一个更大的基于 Arduino 的键盘手，[我们已经见过了，](http://hackaday.com/2015/09/24/arduino-teaches-morse-code/)也是。