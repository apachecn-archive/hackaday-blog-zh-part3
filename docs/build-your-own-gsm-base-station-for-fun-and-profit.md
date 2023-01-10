# 建立自己的 GSM 基站，获得乐趣和利润

> 原文：<https://hackaday.com/2016/04/08/build-your-own-gsm-base-station-for-fun-and-profit/>

在过去的几年里，警察、军队和情报机构使用便携式手机监控设备——俗称“黄貂鱼”——的消息已经传出，尽管他们尽了最大努力来阻止这种做法。有合法的隐私和法律问题，但移动手机站也有一些有趣的技术。

现成的黄貂鱼设备价格在 16，000 美元到 125，000 美元之间，对于一个贫穷的黑客来说太贵了。当然，政府十万美元能做的事，别人五百就能做。[以下是你如何使用现成的硬件建造自己的黄貂鱼](https://evilsocket.net/2016/03/31/how-to-build-your-own-rogue-gsm-bts-for-fun-and-profit/)。

[Simone]一直在玩一个全新的 [BladeRF x40](https://www.nuand.com/blog/product/bladerf-x40/) ，这是一个全双工操作的 USB 3.0 软件定义无线电。售价 420 美元。这一点，结合两个橡胶鸭天线，一个树莓 Pi 3，和一个 USB 电源组是你需要的所有硬件。软件有点复杂，但是西蒙有所有的指令。

当然，如果你想看看这个硬件不太合法的应用，[Simone]的构建只擅长接收/窃听/拦截*未加密的* GSM 信号。如果你想在燃烧的人建立几个基站，像摇头丸一样分发 SIM 卡，这很好，但 GSM 有加密功能。如果不做一点工作，你就无法解密这个系统能看到的每一个 GSM 信号。

幸运的是，全球移动通信系统已经崩溃了。[在 2007 年的 cc camp](http://hackaday.com/2007/08/11/cccamp-2007-gsm-a5-cracking/)，【Steve Schear】和【David Hulton】开始构建一个 A5 密码的彩虹表，用于手机和发射塔之间的 GSM 网络。 [GSM 破解是开源的](http://hackaday.com/2010/07/22/release-the-kraken-open-source-gsm-cracking-tool-released/)，而[GPRS](https://srlabs.de/gprs/)也有漏洞，GSM 网络使用这种方法将数据传输中继到手机。以防你没注意到，GSM 彻底坏了。

谢谢[贾斯汀]的提示。