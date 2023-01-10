# 多核 ZX 频谱

> 原文：<https://hackaday.com/2017/02/16/a-multicore-zx-spectrum/>

从[telmomoya]的博客中，我们发现了他的最新项目:一个基于硬件的用于 ZX 频谱模拟器的多核解决方案。这不是我们第一次展示他的作品，去年我们就在开发一款 [ARM 双核 Commodore C64](http://hackaday.com/2016/07/02/the-dual-core-arm-powered-commodore-64/) 。幸运的是，对于 Speccy 粉丝来说，ZX 频谱项目似乎是不可避免的。

其核心是基于恩智浦 LPC4337 的双核(M4 和 M0) 32 位微控制器 EduCIAA NXP 板。这是阿根廷设计的微控制器板，诞生于阿根廷的学术和工业合资企业。[telmomoya]利用多核架构，在 M4 内核上运行 ZX 频谱仿真器，并通过 M0 内核生成 VGA 信号。这保证了对时间相当敏感的 VGA 生成与仿真和其他内核上运行的任何任务保持隔离。VGA 同步是通过轮询和使用 DMA GPIO 实现的。RGB 信号最高可达 256 色。为了存储 48 kb VGA 帧，使用了一个 AHB32 和一个 AHB16 存储器 IC。

在软件方面，[telmomoya]采用了 Aspectrum，一个完全用 C 语言编写的 ZX 频谱模拟器，根据他的需要进行了修改。总的来说，该项目面临许多挑战和问题，如彩色 VGA 生成(带 GPIO DMA)、TFT SPI 低 fps、进程间通信和总线共享。

你能试着说出演示视频中所有游戏的名称吗？

 [https://www.youtube.com/embed/v_a6dzCKRAI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/v_a6dzCKRAI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

