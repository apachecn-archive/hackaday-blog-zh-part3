# 脂添加到乐高电源功能电源砖

> 原文：<https://hackaday.com/2017/09/10/add-lipo-with-the-lego-power-functions-power-brick/>

乐高的动力功能元件主要由 DC 马达和由这些马达驱动的硬件组成，如齿轮和轮子。它们还包括电池组，通常是一堆装在塑料盒里的 AA 电池。该系统的挑战之一——至少对黑客来说——是与产品线的插头连接，这些插头类似于内置电源和接地连接器的 2×2 板，设计为不可能反向连接。很难制作插头的物理形状，连接器就在它们应该在的地方。这一障碍意味着你还必须使用乐高的动力箱，或者冒险用未经监管的油脂来油炸你的组件。

[LiPo Power Brick](https://hackaday.io/project/27150-lipo-power-brick) 项目用作 DC-DC 电源，提供恒定的 9 V 输出，
过流保护将电流限制在 3 A 峰值或 2 A 持续过放电保护，当电源归零时关闭电源。它可以与 [Sbrick](https://www.sbrick.com/) 智能电源功能控制器配合使用。SBrick 还可以为每个通道提供 3A 的电流，这是任何 LEGO PF 兼容电源都无法提供的。

LiPo Power Brick 与标准的 2×4 brick 大小相同，允许您轻松地将其添加到您的下一个项目中。