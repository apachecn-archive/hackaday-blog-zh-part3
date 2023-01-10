# 32 种灰度

> 原文：<https://hackaday.com/2018/06/06/32-shades-of-gray/>

ATtiny85 是一件不可思议的工程作品。只需八个引脚，你就可以得到一个微控制器，它的力量足以完成一些非常繁重的工作。你得到一个开源工具链，如果你真的很好，你可以建立自己的程序员。尽管它有其局限性；没有很多闪光灯，当然你总是需要一些额外的引脚。

对于他的 Hackaday 奖参赛作品，[danjovic]正在挑战“tiny85”的极限。他用它作为测试模式发生器，向任何旧电视推出像素。整个电路由一个硬币电池供电，整个装置可以放在一个井字盒里。

如你所料，该项目的核心是一个使用所有六个可用引脚的电阻梯，其中五个用于亮度，一个用于同步。如果你继续追踪的话，那就是 32 种灰度。诀窍是使用内部 PLL 和一点数学知识来计算适当的电阻值。结果只是一个测试图案，是的，但是[danjovic]设法得到了一个分辨率为 850 像素的测试图案。以任何标准衡量，那都不坏。

当然，如果你不喜欢灰度，你也可以使用 tiny85 to [通过无线](https://hackaday.com/2015/02/26/attiny85-does-over-the-air-ntsc/)发送不同的颜色，甚至通过 VGA 端口推送卡纸[。](https://hackaday.com/2015/12/17/attiny-does-170x240-vga-with-8-colors/)

The [HackadayPrize2018](https://hackaday.io/prize) is Sponsored by: [![Microchip](img/20eb9d92b47da4c15177567c02a65727.png)](https://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey)  [![Supplyframe](img/2d012d9fc9c7873688699aeadb4742d2.png)](https://supplyframe.com/)