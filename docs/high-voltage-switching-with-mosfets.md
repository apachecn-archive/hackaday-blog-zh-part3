# 利用 MOSFETs 实现高压开关

> 原文：<https://hackaday.com/2018/06/10/high-voltage-switching-with-mosfets/>

使用 MOSFET 作为开关通常非常简单。使栅极电压相对于源极足够大，并且电流流过沟道。然而，如果切换更高的电压，可能需要一些额外的电路来保护器件的栅极，也可能需要驱动整个器件的微控制器。[Lewis]在他最新的一系列关于 MOSFETs 的视频中讨论了[高压开关](http://www.bristolwatch.com/ccs/power_mosfet_switch.htm)。你可以看下面的视频。

您将在视频中看到一个驱动 50 V 负载的试验板设置和一个更高电压的 H 桥。涵盖三大主题:使用光隔离器、使用栅极分压电阻和使用齐纳二极管限制栅极电压。

当然，只要一切正常，无论有无高压，光隔离器都不是必需的。然而，它可以防止高频噪声从 FET 沟道通过充当电容的栅极传导。如果出现使通道与栅极短路的故障，它也有助于保存控制器。

泄放电阻也不是针对高电压的。因为在 DC，栅极实际上是一个开路，所以像这样增加一个电阻是一个好主意，这样当栅极驱动关闭时，你就不必等待栅极上的电荷消散。此外，该电阻还能防止静电放电(ESD)损害，因为 ESD 往往会流经电阻，而不是击穿器件的栅极氧化层。

齐纳以两种方式看待服务。首先，电路利用它从 50 V 电源获得 12 V 电压。然而，在后来的版本中，设计使用它作为箝位，将 P 沟道的栅极保持在 12 V，这两者都很重要，因为栅极的最大额定值是 20 V。

虽然视频中的器件是 IRF630s 和 IRF9630s，但这些原理适用于许多不同类型的 fet。在完成设计之前，请记住您拥有的产品并理解数据手册。

如果你想要更基础的，有很多教程。我们甚至详细研究了[高端开关](https://hackaday.com/2015/09/16/learn-and-build-a-high-side-switch/)。

 [https://www.youtube.com/embed/n3H7y3JhOAk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/n3H7y3JhOAk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

