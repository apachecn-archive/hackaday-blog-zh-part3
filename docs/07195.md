# 用 Skimmer 扫描仪找出骗子

> 原文：<https://hackaday.com/2017/09/25/seek-out-scammers-with-skimmer-scanner/>

上周，我们报道了 Sparkfun 在[逆向工程中所做的一些工作，这是一种安装在汽油泵上的硬件卡套](https://learn.sparkfun.com/tutorials/gas-pump-skimmers)，它包含了卡支付硬件。问题中的设备是一种中间人攻击，PIC 微控制器被编程为侦听读卡器和泵计算机之间的串行通信，然后将结果存储在 EEPROM 中。

这些设备具有蓝牙模块，骗子可以通过该模块远程获取卡的详细信息，这反过来提供了一种在野外识别他们的便捷方法。如果你在水泵处发现一个蓝牙连接，上面有正确的标识和密码，那么通过一个简单的反应测试，就可以认定它是一个盗用者。为了让这变得更加容易，他们编写了一个应用程序，当我们报道它时，它可以从 GitHub 库中获得。

在一次公益活动中，他们现在呼吁硬件黑客和制造商社区今天，9 月 25 日星期一，走到一起，尽可能多地吸引人们对这些野生设备的关注，如果运气好的话，可以关闭一些设备。为此，[他们在谷歌 Play 商店](https://play.google.com/store/apps/details?id=skimmerscammer.skimmerscammer)发布了该应用的编译版，让它非常容易安装到你的手机上，他们正在寻求你的帮助。他们要求人们首先阅读上面链接的教程，然后安装应用程序，并带着它上路。然后，如果你们中的任何人发现了一个 skimmer，请发微博告知，包括你的邮政编码和 [#skimmerscanner](https://twitter.com/hashtag/skimmerscanner?src=hash) 标签。也许有一点时间的人可能会喜欢获取这样的撇油器位置数据并绘制地图。

这将是很好的想法，这项工作可能会引起人们对汽油泵令人震惊的缺乏安全性的关注，这为撇油器提供了便利，扰乱了一些恶棍的财务，甚至导致他们中的一些人免费乘坐警车。不管怎样，我们可以希望。

汽油泵图片:迈克尔·里维拉[ [CC BY-SA 3.0](https://commons.wikimedia.org/wiki/File:BP_Pumps,_US_19,_Jefferson_County.JPG) 。