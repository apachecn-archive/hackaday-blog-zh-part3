# 全速便携的苹果//e

> 原文：<https://hackaday.com/2017/02/21/a-full-speed-portable-apple-e/>

不久前，[Jorj]从 12 月份听到了一个黑客帖子。这是一个在 ATMega1284p 上模拟的手持苹果 IIe。毫无疑问，这是一个令人印象深刻的壮举，但是*完全错了*。这款 ATapple 只有 12k 的 RAM，只能以正确速度的 70%运行。阿塔普尔令人印象深刻，但[Jorj]知道他可以做得更好。他着手创造终极便携式苹果 IIe。[据说，他成功了](https://hackaday.io/project/19925-aiie-an-embedded-apple-e-emulator)。

这个项目和它的灵感有一些共同点。它们都装配在 perfboard 上，使用微型轻触开关作为键盘。该显示器是标准的 TFT 显示器，很容易从易贝、亚马逊或速卖通获得。两者都有一个用于糟糕的 Apple II 音频的扬声器，巨大的 5 1/4 英寸软盘已经缩小到 SD 卡的大小。相似之处到此为止。

[Jorj]知道他需要马力来完成这个构建，所以他转向了他工作台上最强大的微控制器开发板:Teensy 3.6。这是一款 180 MHz ARM Cortex M4，运行全速 Apple IIe 仿真器。编写一个简单的 6502 仿真器很简单，但是 Apple IIe 仿真也需要一个 MMU。完整的仿真器在[Jorj]的报告中可用[，并且通过了](https://github.com/JorjBauer/aiie)[对 6502 功能](https://github.com/Klaus2m5/6502_65C02_functional_tests)的所有测试。

该项目可以轻松运行所有的 Apple II 软件，但我们真的被整个电路的简单所震惊。除了这些小东西，这个建筑真的没什么特别的。这是一个现成的显示器，一个死简单的键盘矩阵，和一点点杂七杂八的电路。它非常简单，可以构建在一块 perfboard 上，我们希望它简单到有人可以克隆电路并共享 PCB。