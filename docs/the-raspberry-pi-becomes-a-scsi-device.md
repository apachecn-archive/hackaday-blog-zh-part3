# Raspberry Pi 变成了一个 SCSI 设备

> 原文：<https://hackaday.com/2017/05/01/the-raspberry-pi-becomes-a-scsi-device/>

自 80 年代以来，从 SUN boxes 到可爱的小型 MAC，数百种不同型号的计算机中都有 SCSI 设备。这些硬盘和光盘正在慢慢消亡，整个一代技术也随之消失。目前，保存这些带有 SCSI 驱动器的计算机的最佳方法是由[Michael McMaster]设计的 SCSI2SD 设备。虽然这款设备确实做到了它所说的功能——将 SD 卡变成 SCSI 链上的驱动器——但它的价格相当昂贵，只有 70 美元。

[GIMONS]有更好、更便宜的解决方案。[这是一个用于 Raspberry Pi](http://www.geocities.jp/kugimoto0715/rascsi/index.html) 的 SCSI 设备仿真器(原文链接失效，[这是这篇文章的新位置](http://retropc.net/gimons/rascsi/index.html))。它只使用一些粘合逻辑和一点代码，就可以将 Raspberry Pi 变成 SCSI 硬盘、磁光驱动器、CDROM 或以太网适配器。

就硬件而言，这是一个非常简单的构建。Pi 上的 40 针 GPIO 连接器通过几个 74LS641 收发器连接到 50 针 SCSI 连接器，收发器带有几个用于上拉和下拉的电阻包。该软件允许虚拟磁盘设备——硬盘、磁光驱动器或 CDROM——从 Raspberry Pi 呈现。还有将以太网放在 SCSI 链上的选项，这是一个有用的附加功能，因为以太网到 SCSI 的转换设备通常很少见且很贵。

官方说法是，[GIMONS]为夏普在 80 年代末开发的 [x68000 计算机](https://en.wikipedia.org/wiki/X68000)建造了这个 SCSI 硬盘模拟器。虽然这些机器在日本很受逆向计算爱好者的欢迎，但它们在其他地方非常罕见——尽管[达夫·琼斯]在一次[拆卸中戴上了手套。从 70 年代到 90 年代，SCSI 在计算机上非常流行，因为 SCSI 是一个标准，所以这个版本应该适用于所有的计算机。](https://www.youtube.com/watch?v=W40qGkp-mEU&feature=youtu.be&a)

如果您的复古计算机不需要 SCSI 驱动器，并且您感觉被排除在驱动器仿真俱乐部之外，那么好消息是也有一个 Raspberry Pi 解决方案:[这个 Hackaday 奖项目将 Pi 变成 IDE 硬盘](http://hackaday.com/2017/04/12/hackaday-prize-entry-real-hard-drives-in-the-raspberry-pi/)。

感谢[Gokhan]的提示！