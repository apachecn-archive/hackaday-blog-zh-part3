# 将轻触开关变成键盘

> 原文：<https://hackaday.com/2018/06/08/turning-tact-switches-into-keyboards/>

在 DIY 电子世界中，一个尚未解决的大问题是小键盘。构建自己的 QWERTY 键盘是一个经过充分研究并完全解决的问题；你只需要看看机械键盘社区就能找到证据。不过，对于一个小键盘，你可能会看到一个旧的黑莓手机，一个蓝牙小玩意，或者滚动你自己的[像神奇的 Hackaday 贝尔格莱德徽章](https://hackaday.com/2018/05/15/retro-computer-badge-for-hackaday-belgrade-has-everything-you-wished-for-back-in-the-day/)。这些都有缺点。你需要为黑莓键盘的带状电缆找到一个接头，标准的蓝牙键盘需要蓝牙，虽然贝尔格莱德徽章的键盘工作良好，但它是一个徽章，而不是一个你会扔在包里使用多年的键盘。

[bobricious]可能已经破解了。为了他的黑客奖参赛作品，[他用轻触开关](https://hackaday.io/project/158454-mini-piqwerty-usb-keyboard)创造了一个微型 USB 键盘。秘诀是什么？一整块电路板。它看起来很棒，而且它可能经得起被扔在一个装满电子产品的随机袋子里的考验。

键盘的电子设备足够简单；有 56 个标准通孔轻触开关和一个 SAMD21 微控制器。通过微型 USB 端口、串行或 I2C 与外界连接。它也很小，长约 5 厘米，宽约 10 厘米。

这里真正的诀窍是使用一堆 PCB 来标记按钮，并提供一点机械支持。这个项目的面板由一个容纳所有电子设备的基板和一个辅助板组成，该辅助板为整个项目提供了一个完整的外观，同时增加了一点结构支撑。

如果你从来没看过小键盘的选项，那就没多少了。黑莓已经是过去式了，没有什么好办法给小项目添加 QWERTY 键盘。这个项目绝对做到了这一点。因为基本的想法是，“在第二个 PCB 上打孔”，这个想法也可以转移到其他键盘布局上。

The [HackadayPrize2018](https://hackaday.io/prize) is Sponsored by: [![Microchip](img/20eb9d92b47da4c15177567c02a65727.png)](https://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey)  [![Supplyframe](img/2d012d9fc9c7873688699aeadb4742d2.png)](https://supplyframe.com/)