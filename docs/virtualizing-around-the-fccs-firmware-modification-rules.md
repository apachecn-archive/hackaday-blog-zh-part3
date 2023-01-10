# 围绕 FCC 的固件修改规则进行虚拟化

> 原文：<https://hackaday.com/2016/06/14/virtualizing-around-the-fccs-firmware-modification-rules/>

去年，[FCC 引入了新法规](https://hackaday.com/2015/08/31/fcc-introduces-rules-banning-wifi-router-firmware-modification/)，要求路由器制造商实施软件安全措施，以限制特定 5GHz 频段的功率输出。政府法规遵循意外后果法则，围绕 FCC 新指令的直接担忧是 WiFi 路由器制造商将做出最容易的工程决策。[今年早些时候，这些担心变成了现实](https://hackaday.com/2016/02/26/fcc-locks-down-router-firmware/),据披露，一家大型路由器制造商没有严格遵守 FCC 的规定，限制了无线电模块本身的输出，而是锁定了整个路由器。

FCC 关于 5GHz 路由器功率输出的规定从来不是一个严肃的问题；毕竟，联邦通信委员会的目标是保持频谱清洁，并可以迫使制造商限制无线设备的功率输出。问题来自制造商如何实施这一规定——防止用户修改无线电模块输出的最简单的解决方案总是防止用户修改整个路由器。开发人员不喜欢它，聪明的用户感到惊恐，甚至联邦通信委员会对其监管的意外后果也有点慌乱。

虽然防止修改无线电模块的最简单的解决方案是防止修改整个路由器，但是还有另一种方法。Imagination Technologies 的人员提出了一个虚拟化方案，允许路由器制造商根据 FCC 指令锁定无线电模块，同时仍然允许使用 OpenWrt 等开源路由器固件。

这款下一代路由器的功能演示来自 [prpl 安全工作组](https://prplfoundation.org/2015/03/17/prpl-foundation-announces-formation-of-security-working-group-to-define-open-framework-addressing-next-generation-security-requirements-of-future-connected-devices/)，它使用 MIPS Warrior CPUs 来创建多个可信环境。路由器的控制可以由一个安全环境来处理，而路由器固件的其余部分——包括 OpenWrt 可以在更有利于开源固件的环境中运行。

一个划分的虚拟化路由器的演示使用了一个开发套件，包括一个运行在 1GHz 的双核 MIPS P5600 CPU 和一个插入 USB 端口的 Realtek RTL8192 WiFi 适配器。WiFi 适配器的驱动程序在一个安全的管理程序下运行，这使得它足够安全，可以通过 FCC 的检查。

如果没有微处理器和微控制器中的硬件虚拟化，这种构建是不可能的。Imagination Technologies 已经在这方面努力了一段时间，就在几年前[展示了一个虚拟化的 PIC32。](https://hackaday.com/2015/09/17/hardware-virtualization-in-microcontrollers/)

在下面的视频中，Imagination Technologies 演示了一个运行三台虚拟机的 MIPS 板。第一台机器运行 OpenWrt，第二台运行 WiFi 驱动，第三台运行第三方应用。使一台机器崩溃不会导致其他机器崩溃，而且根据 FCC 的规定，WiFi 驱动程序被锁定在一个安全的环境中。

虽然很难想象基于 MIPS 板的路由器会比今天路由器中已经很便宜的路由器 SOC 更便宜，但这种安全虚拟化的方法是给消费者带来他们应得的东西的最佳方式:为他们的所有设备提供开源选项。

 [https://www.youtube.com/embed/jJyDvrn3Ahk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/jJyDvrn3Ahk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

