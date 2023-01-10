# Raspberry Pi 零步进驱动器，众多模块中的第一个

> 原文：<https://hackaday.com/2018/07/01/raspberry-pi-zero-stepper-driver-first-of-many-modules/>

总的来说，Raspberry Pi(尤其是 Zero W 型号)是很棒的硬件，但在嵌入式应用中，它们并不完全是即插即用的。用户需要提供稳压电源、操作系统，并注意正确的关断和 ESD 预防措施。尽管如此，这些功能仍然值得考虑，[Alpha le ciel]有一个项目可以通过 [Raspberry Pi Zero W 步进电机模块](https://hackaday.io/project/86834)简化实施，该模块本身是一个更大项目计划的一部分，旨在使 Pi Zero W 成为机器人和 CNC 应用的强大构建模块。

[Alpha le ciel]正在建造这个步进电机模块，作为许多 Raspberry Pi 帽子中的第一个，旨在为 Raspi 提供机器人应用硬件。特别是，该模块具有两个 A4988 步进电机驱动器、一个用于提供 7-20V 电源或电池的连接器，以及一个降压转换器，用于将电源降至 Pi 本身所需的 5V。所有相关的引脚都分散在 Pi 的 GPIO 头上，这使得该模块成为向 Pi 添加一对电机的最简单方式。那是什么意思？打印机或者自平衡机器人，真的随便你。

一个符合 Pi Zero 足迹的步进驱动器是一个好的开始，而创建额外模块的更大概念是一个值得参加 Hackaday 奖的项目。

The [HackadayPrize2018](https://hackaday.io/prize) is Sponsored by: [![Microchip](img/20eb9d92b47da4c15177567c02a65727.png)](https://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey)  [![Supplyframe](img/2d012d9fc9c7873688699aeadb4742d2.png)](https://supplyframe.com/)