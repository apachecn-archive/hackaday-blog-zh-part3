# 先生升级老式电脑娱乐

> 原文：<https://hackaday.com/2017/11/18/mister-upgrades-vintage-computer-recreations/>

MiST 项目为重建老式计算机提供了一个基于 FPGA 的平台。我们最近看到了一个升级版的主板，目标相似，但功能更强。你可以看到一个视频，板的行为像一个苹果][玩吃豆人，如下。

主板没有模拟目标计算机。相反，它使用 FPGA 来托管目标的硬件实现。有苹果，雅达利，Commodore，Coleco，世嘉，辛克莱和许多其他电脑的核心。也有很多街机游戏核心用于像 Defender，Galaga，和 Frogger 这样的游戏。

这位先生使用一块展示 Altera Cyclone V SE 的 Terasic DE-10 板。该 FPGA 具有 110，000 个逻辑元件和大约 5K 位的块 RAM。它还包含两个运行频率为 800 MHz 的 ARM Cortex A9 CPUs。FPGA 和 CPU 可以共享 1gb 的 DDR3 RAM。ARM CPUs 可以引导 Linux，如果您愿意，您可以在软件中模拟一些或所有的东西。虽然有一个 VGA 输出，但也有一个视频缩放器，可以驱动标准的 HDMI 输出。

使 MiSTer 不仅仅是一个 FPGA 演示板的是三个子板(当然，还有软件和 FPGA 配置)。有一个 SDRAM 子板、一个 I/O 板和一个可选的实时时钟板。该项目是开源的，提供了所有的原理图和 Gerber 文件。

I/O 板提供传统 VGA 输出和音频输出(模拟和数字)连接。如果您不想要这些功能，它是可选的。

如果你想比较这两种主板，我们看了原始的模仿麦金塔的薄雾。也许这种设置正是我们需要的[创造从未存在过的计算机](https://hackaday.com/2017/10/13/computers-that-never-were/)。

 [https://www.youtube.com/embed/BOHuxjuYwhw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/BOHuxjuYwhw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

