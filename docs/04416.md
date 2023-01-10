# 混合 Raspberry Pi + PIC32 =示波器和函数发生器

> 原文：<https://hackaday.com/2016/12/13/hybrid-raspberry-pi-pic32-oscilliscope-and-function-generator/>

[PicBerry](http://people.ece.cornell.edu/land/courses/ece4760/FinalProjects/f2016/ak634_jmw483_dm797/ak634_jmw483_dm797/ak634_jmw483_dm797/index.html)是由[Advitya]、[Jeff]和[欧阳丹丹]完成的一个学生期末项目，它采用混合方法来创建一个便携式(且价格合理)的组合数字示波器和函数发生器。它基于 Raspberry Pi，具有直观的 Python GUI，可以同时生成和测量。

但是等等！Raspberry Pi 是一台功能强大的小型 Linux 机器，但满足实时截止日期并不是它的强项。这就是混合方法的用武之地。Pi 负责用户界面和其他功能，SPI 上的 PIC32 用于 1 MHz 采样和以 500 kHz 运行 DAC。将它们结合到 PicBerry 的想法是为了获得两个世界的最佳效果，Pi 和 PIC32 各做自己最擅长的事情。读数分批从 PIC32 发送到 Pi，每 30 ms 更新一次，这样用户就不会感觉到任何明显的滞后。

项目文档指出，可以进行改进，速度与常规的工作台设备相差甚远，软件缺乏一些典型的功能，如触发，但总的来说，对于不到 50 美元的零件来说，还不错。事实上，除了 Raspberry Pi、PIC32 和 MCP4822 数模转换器之外，几乎没有任何组件。下面嵌入了一个简短的演示视频。

 [https://www.youtube.com/embed/RhydIMA4xgQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/RhydIMA4xgQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[Bruce Land]——他曾经创造了一个零 CPU 周期函数发生器——给了我们一个提醒！