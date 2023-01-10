# Hackaday 奖参赛作品:数控 RepRap

> 原文：<https://hackaday.com/2016/06/04/hackaday-prize-entry-a-numerically-controlled-reprap/>

计算机永久存储的故事始于提花机。不如维基百科文章聪明的 Hackaday 评论者可能会争辩说，这是早期的 Bouchon 和 de Vaucanson 织机，但无论如何，我们都应该将永久存储方法归功于织机设计师。因此，故事是这样的，用于在布上编织锦缎和锦缎图案的穿孔卡变成了用于统计人口、计算火炮轨迹的穿孔卡，并以拇指指甲大小的微型 SD 卡中数百千兆字节的存储空间结束。

这个故事掩盖了一个重要的事实。17 世纪的自动织布机只是一种让生产过程更快的方法。这些自动织布机是数控机床的前身。这些机器，首先是车床，然后是磨机和各种金属加工工具，最早出现在 20 世纪 50 年代，使用穿孔带存储从金属中磨出零件所需的命令。就像现代 3D 打印机上的 SD 卡一样。

对于[will.stevens 的] Hackaday 奖参赛作品，他将回到自动化制造的根本[并为他的 3D 打印机](https://hackaday.io/project/11914-relayreprap)制造一个穿孔读卡器。这个想法合理吗？是的。会很容易吗？不，[威尔]正在他的 3D 打印机上制作他的穿孔卡片阅读器。这是 RepRap 自我复制哲学的终极表达，也是一个有趣的工程挑战。

[威尔]的穿孔卡片打印机控制器的想法使用继电器。这是一个简单的控制系统，它对 X 轴和 Y 轴以及一条线的长度进行编码。这台打印机不能在每个方向上打印线条，相反，这台打印机在 360 度中只能使用 48 个可能的角度。在大比例下，打印和绘图会有锯齿，但在小比例下，这个控制系统将能够打印出类似圆形的东西。

[will]有一份他提议的控制系统的 PDF 文件，他已经在努力创建 3D 打印的继电器和螺线管。[will]今年 Hackaday 奖的目标是创造一个 2D 绘图仪——距离 3D 打印机只有一个轴，他正在自己打印打孔卡的路上。

The [HackadayPrize2016](http://hackaday.io/prize) is Sponsored by: [![Atmel](img/2e52aec37df7a9bb2e83735e78e154fe.png)](http://hackaday.io/atmel)  [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](http://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](http://www.digikey.com/)  [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](http://supplyframe.com/)