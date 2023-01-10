# 神经网络万向节一直在观察

> 原文：<https://hackaday.com/2017/10/10/neural-network-gimbal-is-always-watching/>

[加布里埃尔]拿起一台 GoPro 记录他在蒙特利尔的斜坡和小径上的冒险，但很快发现他在镜头前比在镜头后更好。事实证明，他甚至更适合坐在工作台后面，[因为他设计的完全定制的自动跟踪万向架](https://imgur.com/a/mCSWP)简直就是一件艺术品。

这里发生了很多事情，正如你所料，[在【Gabriel】让所有部分一起工作之前，需要几次迭代](https://www.youtube.com/watch?v=8SeI-KrNr7w)。[万向架的主体](https://hackaday.com/2013/03/25/installing-glados-in-the-ceiling-of-your-house/)看起来像 GLaDOS，完全是 3D 打印的，装有马达、摄像头和一系列超声波接收器。做计算重担的[Nvidia Jetson TX1](https://hackaday.com/2015/11/24/the-nvidia-jetson-tx1-its-not-for-everybody-but-it-is-very-cool/)正坐在它自己看起来时髦的 3D 打印外壳中，但【Gabriel】指出，硬件的未来版本应该能够将它们重新结合起来。

在该系统的当前版本中，目标戴着一个超声波发射器，由万向节中的传感器接收。超声波提供的粗略位置信息随后由 Jetson TX1 上运行的神经网络进行[细化，以便摄像机始终聚焦在移动物体上。现在，Jetson TX1 通过 WiFi 从摄像机获取视频，并通过蓝牙命令万向节硬件。然而，一旦 Jetson 进入万向架，一些硬件可能会直接连接，并且[Gabriel]说超声波可能会从设计中完全删除，以利于纯软件跟踪。他计划将这个项目开源，但他说在他揭开面纱之前，他还有一些内部事务要做。](https://hackaday.com/2017/05/22/wrap-your-mind-around-neural-networks/)

从最简单的到[舒适奢华的](https://hackaday.com/2016/02/29/pretty-gimbal/)，临时搭建的相机支架已经成为摄影黑客的某种通行权利。但是在这个项目中，看起来标准变得更高了。

 [https://www.youtube.com/embed/t9-Enawv_mY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/t9-Enawv_mY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

