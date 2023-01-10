# 宜家站立式书桌在林巴士上从“笨”变“聪明”

> 原文：<https://hackaday.com/2017/02/10/ikea-standing-desk-goes-dumb-to-smart-with-lin-bus/>

宜家产品以干净、斯堪的纳维亚设计和低成本而闻名，但正是它们的 DIY 或“自己组装”功能让它们如此受黑客欢迎。我们似乎经常收到关于宜家黑客的提示。[Robin Reiter]有一张 Bekant 坐/站电动桌，上面有按钮可以升高和降低桌面，但没有任何记忆预设。这很遗憾，因为每次都需要对向上/向下按钮进行大量的修改才能使其正确。按下一个按钮，去拿杯咖啡，然后回来，发现它已经被调整到了理想的高度，这感觉很好。通过一点点黑客攻击，他不仅可以添加内存预置按钮，还可以添加一个 USB 接口用于未来的计算机控制。

现有硬件由一个 PIC16LF1938 微控制器和一个 [LIN 总线](https://en.wikipedia.org/wiki/Local_Interconnect_Network)协议组成，pic 16 lf 1938 微控制器带有两个用于运动控制的按钮，LIN 总线协议与带有集成编码器的汽车级电机通信，编码器可报告位置值。用他的示波器和分析器嗅了一会儿后，他能够找出马达运动的控制代码。然而，由于一些奇怪的原因，LIN 信号被反转，所以他不得不在 PIC 主机和 Arduino Nano 之间引入一个晶体管信号反相器，作为 LIN 的从节点。由于[Zapta]为 [LIN 总线信号注入器](http://hackaday.com/2014/04/19/a-lin-bus-signal-injector/)开发的 Arduino 库，软件变得更加容易，现在控件有四个按钮——两个用于复制原始的上/下移动，另外两个用作记忆预设。

代码、原理图和一个简单的布线图发布在 [Github](https://github.com/robin7331/IKEA-Hackant) 上，以防有其他人想要复制这个黑客。休息之后，看看他演示代码的视频。

 [https://www.youtube.com/embed/AB75AxprXqQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/AB75AxprXqQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

