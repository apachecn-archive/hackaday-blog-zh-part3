# 控制主电源 Rube Goldberg 风格

> 原文：<https://hackaday.com/2015/09/21/controlling-mains-power-rube-goldberg-style/>

[g3gg0]有一些不错的无线电设备，包括一个 AOR AR-5000 接收机和一个 HiQ SDR。它们太漂亮了，看起来好像没有开关。[g3gg0]厌倦了拔掉电源插头，决定用一个开关来改造他的桌子，这个开关可以为他打开和关闭他的设置。他决定通过 Digispark 板模拟键盘上的滚动、数字和大写锁定 led 来完成这项任务。他使用 led 向 Digispark 发出命令，允许他控制位于它和 AC 之间的 5V 继电器。

从 Digispark 上的一些 USB 键盘仿真代码开始，他对其进行了调整，这样他就可以使用滚动锁定 LED 作为一种芯片选择。一旦按下此按钮，他就可以使用 Caps Lock 和 Number Lock LED 向 Digispark 发出命令。

它被设定总共只能开 5 个小时，以防他忘记关。让我们知道你对这个有趣的方法的想法。