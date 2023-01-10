# 对单价打印机进行逆向工程

> 原文：<https://hackaday.com/2017/06/20/reverse-engineering-the-monoprice-printer/>

当 Monoprice MP Select 迷你 3D 打印机去年发布时，它是一个游戏规则的改变者。是的，这是一台售价 200 美元的打印机，但它也有一个不太明显的秘密:一个没有人见过的 3D 打印机控制器板，由 32 位 ARM 微控制器供电，带有处理 UI 的 ESP8266。这是 3D 打印世界中一套改变游戏规则的电子设备，现在，终于，[有人正在对它进行逆向工程](https://hackaday.io/project/25518-reverse-engineering-the-monoprice-mp-select-mini)。

[Robin]通过将示波器的引线连接到主控制器和显示控制器之间的串行线上，开始了逆向工程。波特率很奇怪(500 kHz)，但除此之外，命令很容易以人类可解析的文本出现。MP Mini 打印机内置了一个网络服务器，在检查了这台打印机提供的网页后，[Robin]发现可以直接从控制板发送 g 代码，获取 SD 卡上的文件列表，并使用 3D 打印机做任何您想做的事情。

在解构了显示板上的电路后，[Robin]发现了你对这样一个简单电路板的预期:一个由 ESP 驱动的 SPI 显示器，以及一个位于旁边的大闪存芯片。[Robin]找到了显示器的模型，并在 Platform.io 上快速构建了一个项目，将文本绘制到 LCD 上。这并不是项目的结束——在这台打印机使用定制固件打印零件之前，还有很多工作要做。

虽然这不是对 MP Mini 内部驱动板的攻击，但这并不是一个真正的问题。这台打印机中的电机驱动板实际上不需要任何改变，并且在去年这台打印机发布时就已经领先了。与大多数事情一样，UI 是弱点，升级该打印机的固件和内置 web 服务器是最好的前进方式。

[Robin]制作了一个非常棒的视频，展示了他是如何逆向设计这个显示控制器的。你可以看看下面。

 [https://www.youtube.com/embed/T-o-ibGUEoA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/T-o-ibGUEoA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

