# 步进电机机器人手臂移动平稳

> 原文：<https://hackaday.com/2018/01/22/stepper-motor-robot-arm-has-smooth-moves/>

[Tobias Kuhn]看过 YouTube 上一个关于使用伺服电机的机器人手臂的视频，他想自己试着做一个。但他发现很难从伺服系统中获得缓慢或平稳的运动。即使移除微控制器并尝试使用 Arduino Nano 上的伺服驱动器 IC 和电位计，也没有让他满意。

然后他找到了非常实惠的 28BYJ-48 步进电机。经过一些实验，他设计出了一个平稳移动的机械臂，它有四个步进器，由 Arduino Mega 和 A4988 步进电机驱动器控制。他没有自己编写一堆步进电机代码，而是在 Arduino 上安装并运行了 grbl 的[四轴分支，将它变成了步进电机控制器。一个小问题是，A4988 电机驱动器用于双极步进电机，但 28BYJ-48 步进电机是单极的。幸运的是，他知道一个非常简单的方法，我们的[Brian Benchoff]写了这个方法，将](https://github.com/dguerizec/grbl-Mega-4axis)[的单极电机变成双极电机](https://hackaday.com/2014/07/29/changing-unipolar-steppers-to-bipolar/)。

为了告诉机器人手臂做什么，他用电位计代替步进电机建造了一个复制手臂。当他操纵复制品时，电位计的值由 Raspberry Pi 和一些自定义 Python 代码读取，这些代码将适当的 g 代码发送到 Arduino/grbl 控制的机器人手臂。有一点滞后，但当他移动复制手臂时，机器人手臂会做同样的动作。请观看下面的视频。

 [https://www.youtube.com/embed/1e5vRpODASk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/1e5vRpODASk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[托拜厄斯·库恩]的机器人手臂并不是我们在这里看到的唯一步进驱动的平滑移动器。看看这个，它增加了一个与一个移动相当迅速的伺服电机驱动的机器人手臂的并排比较。