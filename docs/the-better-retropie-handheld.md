# 更好的复古手持设备

> 原文：<https://hackaday.com/2018/04/07/the-better-retropie-handheld/>

树莓派已经成为这个星球上最好的视频游戏机。有了 RetroPi，任何人都可以玩超级马里奥 3，马里奥医生，甚至 Doki Doki Panic。Adafruit 的 PiGRRL Zero 和[【Wermy】对一个旧的砖块游戏男孩的重新构造](https://www.sudomod.com/game-boy-zero-guide-part-1/)使 Raspi Zero 和显示器变得便携，还有我们非常喜欢的所有复古游戏。

然而，这些构建有一个问题。他们只使用 Raspberry Pi Zero，这限制了仿真性能，而且 Raspi 3 对于便携式控制台来说太大了。有什么解决办法？这是有史以来最伟大的自制游戏机。对于今年的 Hackaday 奖， [[DeanChu]正在建造 Retro-CM3](https://hackaday.io/project/94791-retro-cm3-a-powerful-retropie-handled-game-consol) 。这是一款带有 3D 打印外壳的复古手持设备，由 Raspberry Pi 计算模块 3 提供支持。伙计们，往后站。我们有一个赢家，将超越树莓派*和* 3D 打印子编辑器。

当然，这个版本的关键特性是 [Raspberry Pi 计算模块 3](https://www.raspberrypi.org/products/compute-module-3/) 的原始处理能力。这是一个装有 4gb eMMC 的覆盆子 Pi 3，它被塞在一个适合 SODIMM 插座的板上。该设备上的引脚使您可以访问 GPIOs 和 DSI 连接器。要把它变成一个令人惊叹的复古仿真控制台，你真正需要的是一个带有几个按钮、电源和显示器的分线板。

此版本的额外组件包括一个使用 DPI 接口的 3.2 英寸 LCD。有一个扬声器和一个 2000 毫安的电池。这里真正棘手的部分是定制的 PCB，断开计算模块上的 DPI 引脚，添加一个小扬声器，并抛出一个小 STM32 来读取按钮。这是一个完整的系统，随时可以装入 3D 打印的外壳中。

简单地说，这是你见过的最好的便携式 Raspberry Pi，至少在我们得到具有 Pi 3 功能的 Rasberry Pi Zero 之前是这样。这是对非常小的计算模块的出色使用，也是我们迄今为止看到的最精美的 Hackaday 奖参赛作品之一。

The [HackadayPrize2018](https://hackaday.io/prize) is Sponsored by: [![Microchip](img/20eb9d92b47da4c15177567c02a65727.png)](https://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey)  [![Supplyframe](img/2d012d9fc9c7873688699aeadb4742d2.png)](https://supplyframe.com/)