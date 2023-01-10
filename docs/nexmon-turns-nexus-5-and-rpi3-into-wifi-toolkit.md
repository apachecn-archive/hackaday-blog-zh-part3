# Nexmon 转 Nexus 5(还有 RPi3！)到 WiFi 工具包中

> 原文：<https://hackaday.com/2016/09/08/nexmon-turns-nexus-5-and-rpi3-into-wifi-toolkit/>

回到过去，当 wardriving 仍然有用的时候(阅读:在 WPA2 广泛传播之前)，我们经常在口袋里带着一头 Zaurus 四处游荡，运行 Kismet。今天，每部手机都有 WiFi，并且内置了一个更强大的处理器。但是，唉，固件被锁定了。

![mrmcd16-7748-deu-nexmon_-_make_wi-fi_hacking_on_smartphones_great_again_sdmp4-shot0005_thumbnail](img/e9416bf805540aa119c6067c4ca30d46.png)进入[耐克蒙项目](https://dev.seemoo.tu-darmstadt.de/bcm/bcm-public)。如果你有一部采用 Broadcom BCM4339 WiFi 芯片组的 Nexus 5 手机，你现在就有了一台监控模式、数据包注入的老爷车，它看起来比旧的 Zaurus 少得多。但更重要的是，NexMon 是开放的。如果你想深入了解在手机 WiFi 上逆向设计一个洞的过程，或者制作自己的补丁，[这里是一个很好的起点](http://arxiv.org/abs/1601.07077)。

但是等等，还有呢！最近发布的 Raspberry Pi 3 有一个类似的 Broadcom WiFi 芯片组，并得到了同样的待遇，将你的 RPi 3 变成了一个无线嗅探发电站。有多少树莓派“黑客”真的黑了树莓派？嗯，这里有一个。

我们第一次听说这个项目是在上周末举行的 MetaRhein-Main Chaos Days 会议上。 [NexMon 讲座](https://media.ccc.de/v/MRMCD16-7748-nexmon_-_make_wi-fi_hacking_on_smartphones_great_again)(德语，但有英语幻灯片)只是众多讲座中的一个，所有这些讲座都可以在[在线](https://media.ccc.de/c/mrmcd16)上获得。

然而，NexMon 项目是一个突出的例子。他们不仅逆转了 Nexus 5 中的 WiFi 固件，还向您展示了如何逆转，然后将相同的方法应用于 RPi3。对[马蒂亚斯·舒尔茨]、[丹尼尔·韦格默]和[马蒂亚斯·霍利克]的称赞是三倍！