# 注定失败的恒温器

> 原文：<https://hackaday.com/2017/05/22/doomed-thermostat/>

游戏《毁灭战士》被移植到这么多东西上，真是令人惊讶。再输入一个端口，这里的硬件是 Honeywell Prestige 恒温器。

在他的视频中，[cz7asm]向我们展示了游戏在 480 x 272 的 LCD 上运行得非常好，NES 控制器插入了原本用于软件更新的 USB 端口。恒温器运行在 STM32F429 上，这是一个 ARM9 处理器，有能力实现它。正在使用的 Doom 引擎是基于游戏的开源端口[巧克力 Doom](https://www.chocolate-doom.org/wiki/index.php/Chocolate_Doom) ，二进制可以下载用于 Windows 和 Mac。源代码也可以下载，供您随意修改。这个由[cz7asm]开发的项目是由[flopps]在 GitHub 上的一个[代码扩展而来的，它原本是为 STM32F429IDISCOVERY 评估板开发的。](https://github.com/floppes/stm32doom)

作者在 [Dropbox 上以 zip 文件](https://www.dropbox.com/s/xy6qjabfuqq24pm/doomostat.zip?dl=0)的形式分享了他的 STM32F4 代码，为了编译它，使用了用于 GNU GCC 的 [Atmel BSP。下面的视频演示了黑客的行动，虽然还没有声音，但这种修改带来的满足感本身就是一种回报。](http://www.atmel.com/tools/sam9g35softwarepackage.aspx)

你还能在什么上面运行毁灭战士？一个[计算器](http://hackaday.com/2012/01/19/doom-for-your-calculator-gets-a-color-upgrade/)或者[英特尔爱迪生](http://hackaday.com/2015/01/10/running-doom-on-the-intel-edison/)甚至 [ATM 机](http://hackaday.com/2014/07/26/playing-doom-on-an-atm/)怎么样！如果有一个处理器有足够的肌肉力量，黑客会找到一种方法在它上面运行 Doom。那么你最近有没有看到任何你认为可以被黑的外星电脑？

 [https://www.youtube.com/embed/2T5LyEjLfP8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/2T5LyEjLfP8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

