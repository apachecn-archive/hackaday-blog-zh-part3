# Hackaday 大奖参赛作品:DIY 6 轴微型机械手

> 原文：<https://hackaday.com/2017/07/04/hackaday-prize-entry-diy-6-axis-micro-manipulator/>

[大卫·布朗]的黑客日奖参赛作品是一种工具的设计，这种工具通常只作为一件昂贵的工业设备而存在；换句话说，超出了普通实验者的能力范围。这个工具是一个 [6 轴微型机械手](https://hackaday.io/project/25307)，本质上是一个小型机器人执行器，能够进行非常小、非常精确的运动。它使用 3D 打印零件和低成本组件。

![](img/cb672ea886a48fda96a7930b5f683b9a.png)

SLS Nylon Actuator Frame. Motor anchors to top right, moves the central pivot up and down to deflect the endpoints.

该操纵器由六个相同的致动器组成，每个致动器都由单片 SLS 3D 打印尼龙组成，带有定制的 PCB 以控制电机和读取位置反馈。马达移动 3D 打印组件的中心枢轴点，这反过来会使整个零件发生少量偏转。通过固定一个点并连接另一个点，可以实现少量的高度可控的运动。总共六个致动器形成一个 [Gough-Stewart 平台](https://en.wikipedia.org/wiki/Stewart_platform)用于移动工具架。

有趣的是，这个 6 轴微操作器是一个侧面项目。[David]对创建自己的数字紫外线曝光器很感兴趣，这需要使用带有光纤尾纤的紫外线激光二极管。在工业环境中，通过用微型操纵器操纵光纤，根据经验确定光纤相对于激光二极管的最佳位置，然后在粘接到位的同时保持光纤稳定。看到在实验室或工业环境之外的任何地方都明显缺乏微型机械手，并认识到在他自己的需求之外会有应用，[David]决定建造一个。

The [HackadayPrize2017](https://hackaday.io/prize) is Sponsored by:[![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Texas Instruments](img/3734f1c96ffff85ea2a7eaddc92844ba.png)](https://hackaday.io/ti)