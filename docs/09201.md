# 完全从头开始构建的电子速度控制器

> 原文：<https://hackaday.com/2018/04/19/completely-scratch-built-electronic-speed-controller/>

驱动无刷电机需要特定的顺序。为了获得最佳结果，您需要闭合环路，以便电路能够在正确的时间应用正确的序列。您可以使用稍微复杂的电路并监控电机线圈的电气行为来计算时间。或者您可以使用传感器来检测电机的位置。许多电机都内置了传感器，[electronio OBS]在最近的视频中展示了如何[驱动其中一个电机](https://www.youtube.com/watch?v=G9PHqN9vmVI)，你可以在下面观看。如果你想了解如何使用电机线圈作为传感器，他之前在做了一个关于这个主题的[视频。](https://www.youtube.com/watch?v=8LXPcJD6hEA)

有问题的马达是从光驱中取出来的，并带有三个霍尔效应传感器。这些传感器大大简化了驱动电子设备。

带传感器的普通电机具有受调节的传感器输出，但由于这是一个垃圾箱突袭部件，霍尔效应传感器需要一些电路来驱动和读取它们。一个简单的 LM324 比较器和几个电阻就可以解决这个问题。

驱动电路只是几个 MOSFETs，形成三个 H 桥电路。诀窍是如何排序线圈，使你得到你想要的旋转。该视频有一些非常好的动画，解释了所涉及的序列和关键时间。

如果你决定复制电路，请注意，视频有一些反向二极管。您可以在相关网站上找到更新的原理图。

如果你手边没有无刷 DC 马达，你可以随时从垃圾中制造自己的 T1。如果你有一台 3D 打印机，你可以[造一台更好的](https://hackaday.com/2017/05/08/powerful-professional-brushless-motor-from-3d-printed-parts/)。

 [https://www.youtube.com/embed/G9PHqN9vmVI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/G9PHqN9vmVI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

