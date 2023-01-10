# 不带火车的 Mag Lev(但带有 FPGA)

> 原文：<https://hackaday.com/2016/06/26/mag-lev-without-the-train-but-with-an-fpga/>

总是让我们惊讶的是，磁悬浮似乎有两个主要用途:火车和玩具。获得浮动蓝牙扬声器、地球仪或者仅仅是用于展示的浮动平台是相当便宜的。这个想法相当简单，尤其是如果你只关心二维的悬浮。你让一个电磁铁拉动悬浮的物体(当然是含铁的)。当物体达到一定高度时，传感器会检测到并关闭磁铁。物体落下，磁铁重新打开，重复这个过程。如果你做对了，物体会达到平衡，在传感器附近悬停。

康奈尔大学的一些学生决定[使用 Altera FPGA](https://people.ece.cornell.edu/land/courses/ece5760/FinalProjects/s2016/crl233_gp348_nds55/gp348_crl233_nds55/gp348_crl233_nds55/index.html) 实现产生悬浮的控制回路。一个感应传感器确定了一个铁球的位置。该器件使用标准的比例积分微分(PID)控制环路。控制环路和 PWM 产生发生在 FPGA 硬件中。你可以在下面看到他们结果的视频。

然而，该团队还想在 VGA 屏幕上显示数据。虽然没有计算机也可以做到这一点，但为这项任务编写一些软件要容易得多，因此该设备具有嵌入式 NIOS II 处理器内核，可以处理包括显示数据和更改 PID 常数在内的任务。

这个项目是一个很好的例子，它将 FPGA 逻辑和 CPU 结合起来，前者实现了高速，后者实现了更简单的开发。传感器和其他因素意味着球没有很好的横向控制，所以该设备使用一根管子来约束球。

悬浮扬声器和地球仪通常在悬浮部分使用一个强永磁体，并使用四个磁体进行横向平衡。我们[已经看到用 Arduino 做到了](https://hackaday.com/2015/11/02/magnetic-levitation-with-arduino/)。对于真正喜欢冒险的人来说，你可以[在没有任何电子设备的情况下悬浮一个旋转的磁力陀螺](https://hackaday.com/2011/07/23/frustrating-fun-with-magnetic-levitation/)。诚实。

[https://player.vimeo.com/video/167056844](https://player.vimeo.com/video/167056844)