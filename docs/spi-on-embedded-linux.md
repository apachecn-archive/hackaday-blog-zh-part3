# 嵌入式 Linux 上的 SPI

> 原文：<https://hackaday.com/2017/02/19/spi-on-embedded-linux/>

你已经习惯使用串行外设接口(SPI)器件并寻求挑战了吗？我们怀疑你们中的许多人已经接触了 8 位到 32 位微控制器，但是你们花了多少时间在嵌入式 Linux 上玩硬件接口呢？这是一个新的任务，如果你选择接受的话。[Matt Porter] [在 FOSDEM 2017 的演讲中详细介绍了 Linux SPI 子系统](https://fosdem.org/2017/schedule/event/kernel_spi_subsystem/)。为什么不拿一块嵌入式 Linux 板，试着将一些额外的硬件连接到 SPI 总线上呢？

硬件方面正是您所期望的任何嵌入式 SPI:MOSI、MISO、时钟和从机选择。[Matt]简要概述了 SPI 和读取数据手册。如果你需要[掌握所有 SPI 基础知识](http://hackaday.com/2016/07/01/what-could-go-wrong-spi/)，我们自己的【埃利奥特·威廉姆斯】在挖掘基础知识和最常见的陷阱方面做得非常出色。

在视频的 18:30 分左右，当[Matt]跳到 SPI 的 Linux 端时，演讲中有趣的细节开始了。你需要一个控制器驱动和一个协议驱动。控制器驱动程序负责处理引脚(实际硬件)，协议驱动程序负责理解进出的 SPI 数据包(包含任意数量传输的消息)。换句话说，控制器驱动只需要位，并把它们推入或推出硬件，协议驱动使这些位对 Linux 系统有意义。

将 SPI 设备(比如 LCD 和传感器)添加到您自己的嵌入式系统中意味着告诉操作系统关于该硬件的细节，比如最大速度和 SPI 模式。有三种方法可以解决这个问题，但是设备树是现代系统的首选方法。这为控制器驱动程序铺平了道路，它实现了一个 API 集，Linux SPI 子系统将使用该 API 集与您的新硬件一起工作。

协议驱动遵循标准的 [Linux 驱动模型](https://wiki.linuxfoundation.org/tab/linux-device-driver-model)，非常简单。有了这两个驱动程序，新设备就可以连接到操作系统，并开放常见的 SPI API 调用:spi_async()、spi_sync()、spi_write()和 spi_read()以及其他一些调用。

 [https://www.youtube.com/embed/gFPIQ_PlVEY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/gFPIQ_PlVEY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



这对我们来说听起来很有趣，但是如果你觉得有点难以理解，你可以讨论另一个有趣的话题:[使用直接内存访问(DMA)来满足你的 SPI 需求](http://hackaday.com/2016/09/26/pic32-dma-spi/)。

[谢谢提醒德鲁]