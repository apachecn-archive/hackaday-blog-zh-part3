# NanoPi 星团安静、凉爽，并且有闪亮的灯光

> 原文：<https://hackaday.com/2018/07/05/nanopi-cluster-is-quiet-cool-and-has-blinky-lights/>

我们之前已经看过来自英国的[Nick Smith]的超级计算机集群工作，但是他的最新构建非常可爱。这一次，他用 nano Pi fire 3 组装了一台 96 核超级计算机，nano Pi fire 3 是树莓 Pi 的替代品，其内核数量是 T2 的两倍。他的文章向你展示了他是如何构建超级计算机集群的，从设计激光切割丙烯酸外壳到布置电源电缆。

不过，最精彩的部分是他制作了一个可爱的前面板健康显示器。使用 [Pimoroni PHat，](https://shop.pimoroni.com/products/unicorn-phat)显示屏显示 12 块板中每块板的 CPU 负载、温度、磁盘&网络活动，仅使用来自其中一块 NanoPi 板的单条 SPI 电缆。该板运行一个 [Mosquito MQTT 服务器](https://mosquitto.org/)，该服务器每秒钟轮询一次来自每个板的状态信息，然后更新显示，因此应该可以很快发现任何问题。这很重要，因为[尼克]想保持建筑安静，所以他使用了两个几乎无声的风扇，通过控制电压来调节。不过，这不是一个贪婪的集群，因为[Nick]发现它在全速运行时只使用了 55W，在空闲时只使用了 24W。这是另一个简洁的构建，这篇文章有助于你理解为什么(尼克)会以某种方式做事。因此，对于任何对如何规划和构建 SBC 系统感兴趣的人来说，这都是一本好书。你也应该看看尼克以前的作品，比如 SBCs 的[激光切割案例和他的](https://hackaday.com/2018/02/04/a-few-laser-cut-cases-for-your-sbcs/)[树莓 Pi 集群](https://hackaday.com/2016/05/26/raspberry-pi-cluster-build-shows-how-and-what/)。