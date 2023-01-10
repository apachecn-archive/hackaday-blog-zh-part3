# 一个辛辣的再生接收器

> 原文：<https://hackaday.com/2016/03/02/a-spicy-regenerative-reciever/>

我们最近贴了一个关于使用 LTSpice 仿真电子电路的三部分系列([一](http://hackaday.com/2016/02/26/adding-spice-to-your-workbench/)、[二](http://hackaday.com/2016/02/29/spice-power/)、[三](http://wp.me/pk3lN-O26))。你可能会发现自己在想:你真的能用这个程序模拟实际的设计吗？这个对[QRP 盖金的] [极简再生接收器](http://qrp-gaijin.blogspot.com/2015/08/a-12-volt-vackar-style-minimalist.html)的快速分析说“是”。

接收器设计的既定目标(来自[Gaijins]帖子)是:

1.  设计并实现一个极简但实用的再生接收机，能够接收 3-30 MHz 的高频信号。
2.  使用电路仿真工具 LTspice 分析接收机工作的关键方面(例如再生检波器的行为、AF 放大器的增益和频率响应)。
3.  详细解释设计和 LTspice 分析技术，以便感兴趣的读者可以重现仿真结果。此外，为再生检测器或再生接收器的改进设计提供一些参考。

LTSpice 模拟了收音机的再生控制、检测器的稳定性和音频放大器。完全由 2N3904 晶体管(和一个用于调谐电容的变容二极管)构建的无线电按预期工作。

我们报道过[QRP·盖金的]日记，当时他正在制作这台收音机的早期版本。不过，将所有这些放在一个地方并进行扩展是受欢迎的。这可能不是我们讨论过的[最漂亮的再生接收器](http://hackaday.com/2015/09/15/radio-receiver-or-art-why-not-both/)，但它肯定是分析得最好的，它是在实际项目中使用 LTSpice 的一个很好的例子。

 [https://www.youtube.com/embed/LB8ISlB8bZE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/LB8ISlB8bZE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

