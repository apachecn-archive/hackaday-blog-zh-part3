# Hackaday 奖品入口:由 AVR 驱动的 PC-XT 克隆

> 原文：<https://hackaday.com/2017/05/21/hackaday-prize-entry-a-pc-xt-clone-powered-by-avr/>

你阅读这篇文章的设备很有可能是广义的个人电脑。多年来，熟悉的 x86 架构和外设标准已经击败了所有竞争对手，以至于它只是在个人计算的移动和平板电脑领域没有占据主导地位。

拥有多核处理器和 64 位指令集的现代个人电脑与 20 世纪 80 年代早期的 16 位电脑相比已经大相径庭。那些早期的 PC 是当时的计算机，外围设备相对较少，微处理器总线几乎是直接暴露的，而不是通过我们今天期望看到的抽象和看门人。不过，带有 8 位外部总线的 8088 处理器是最原始的 PC 处理器，在合理的范围内，你会发现在那些最早的 IBM 机器上为 DOS 编写的软件仍然经常在你的多处理器庞然大物上运行，在你今天的操作系统上有一个类似 DOS 的层。这 35 年多来几乎没有中断的兼容性链既是一个非凡的工程壮举，也是现代 PC 硬件和操作系统开发人员的沉重负担。

这些早期的个人电脑引起了[Soto . Eric]的注意，他提出了一个有趣的项目[，将 AVR 微控制器与早期个人电脑之一的 8088 系统总线连接起来](https://hackaday.io/project/18868-improbable-avr-8088-substitution-for-pcxt)。因此，所有这些个人电脑的外围设备都可以在更先进的设备的控制下运行。当你考虑到 8088 运行在一个适度的 300 千位，而 AVR 能够运行在一个相对快得多的 22 千位，这个想法是，它应该能够以同样的速度模仿 8088，如果不是更快的话。他的进步使[成为一个漫长而迷人的阅读](https://hackaday.io/project/18868/logs)，到目前为止，他已经可靠地访问了 PC 的 640 kb RAM，与 ISA 总线并行端口进行了对话，并使 CGA 卡产生了颜色和字符。有趣的是，AVR 具有 8088 无法实现的速度提升潜力，例如，它可以使用自己的内部 UART，其指令比访问 PC UART 的指令少得多，并且其内部闪存可以包含 PC BIOS，读取速度比实际 PC 硬件上的实际 BIOS ROM 快得多。

如果你想知道 8088 电脑的用途，看看这个令人印象深刻的演示吧。你自己没有吗？[造一个](http://hackaday.com/2017/04/14/build-your-own-pc-really/)。

The [HackadayPrize2017](https://hackaday.io/prize) is Sponsored by:[![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Texas Instruments](img/3734f1c96ffff85ea2a7eaddc92844ba.png)](https://hackaday.io/ti)