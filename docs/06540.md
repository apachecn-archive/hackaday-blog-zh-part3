# 没有 UART 的反向通道 UART

> 原文：<https://hackaday.com/2017/07/18/backchannel-uart-without-the-uart/>

任何使用过微控制器的人都熟悉使用`printf`作为临时调试器。这种方法称为跟踪，但有一个限制，即它会耗尽一个 UART 外设。信不信由你，有 8051 种变体只有一个串行块，如果你的应用需要它来与另一个设备通信，那你就倒霉了。

[Jay Carlson]有一种方法，他可以通过片上调试器搭载这些跟踪消息。虽然较新的 ARM Cortex-M 软件调试器已经有了这个功能，但[Jay Carlson]的 hack 是为 SiLabs EFM8 控制器设计的。这个想法是将这些调试消息写到 RAM 中一个预定义的位置，调试器无论如何都可以访问这个位置。他的应用程序轮询内存的某个区域，当它找到有效信息时，它读取数据并将其发送到一个专用窗口。它使用调试器作为权宜之计`printf`！

[Jay Carlson]使用 slab8051.dll 接口，将 C#程序和 GUI 放在一起，与 SiLab 的 ide 一起工作。代码可以在 GitHub 上找到，如果你正在使用 EFM8 并且需要帮助，你可以查看一下。这个想法很简单，可以通过多种方式移植到其他控制器上，比如 MSP430。对于那些喜欢 Teensy 的人来说，你可能想看看[在 Teensy](http://hackaday.com/2017/05/01/adding-a-debugger-to-a-teensy-3-53-6/) 3.5/3.6 中增加了调试器支持。