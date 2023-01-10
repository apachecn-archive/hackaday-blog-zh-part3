# 新零件日:ST 的 32 位 3D 打印机控制器

> 原文：<https://hackaday.com/2016/07/19/new-part-day-sts-32-bit-3d-printer-controller/>

有几个 32 位基于 ARM 的 3D 打印机控制器板，如 Smoothieboard，Azteeg X5 mini，[Traumflug]的 Gen5 electronics，Monoprice MP Mini Select 中的任何板，以及其他几个我将被批评没有提到的板。所有这些 ARM 板都提供了更平滑的加速、更好的控制，并最终从它们控制的任何 3D 打印机中获得更好的打印效果。现在，出乎意料的，有一个新的董事会。[这是来自 ST](http://www.st.com/content/st_com/en/products/evaluation-tools/solution-evaluation-tools/computer-and-peripherals-solution-eval-boards/steval-3dp001v1.html) 的评估板，很像那些著名的 Discovery 板，它将自己推销为 3D 打印机的即插即用解决方案。

该板的核心是 STM32F401，它不是 STM32 系列之王，也不是最快的 ARM 微控制器，但任何速度更快或功能更强的产品都会大大增加该板的 BOM。该控制器板具有六个 ST 的 L6474 电机驱动器，其电流足以支持一些结实的 NEMA 23 步进电机，一个多区域加热床，以及 WiFi 模块和外部 LCD 和键盘的连接。你现在可以花 118 美元买到这块板。这块板子不是游戏改变者，但它是游戏被改变的证据。

与所有 3D 打印机控制器板一样，有几个方面会让用户想要更多。这是一个用于 12V 加热器的板(除了床，它有 24V，20A 的输出)，步进驱动器只能达到 16 微步。也就是说，没什么好抱怨的。该产品配有一个名为 [Marlin4ST](https://github.com/St3dPrinter/Marlin4ST) 的 32 位固件。快速浏览一下，看起来像是熟悉的 configuration.h 仍然存在，并且仍然做它应该做的事情。

这种 ST Discovery 板功能非常强大，现在就可以买到，而且相对便宜，但这并不是真正的大问题。这个主板代表的是一个 32 位基于 ARM 的打印机控制器的*参考设计*和*工作固件*。这就是未来，有了这个主板，未来可能会来得更快一些。

感谢[jagerboots]发送此邮件。