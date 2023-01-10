# 为娱乐定制 30 美元的 ip 摄像头

> 原文：<https://hackaday.com/2018/03/05/customising-a-30-ip-camera-for-fun/>

如今，像许多其他设备一样，WiFi 相机也配备了某种 Linux 子系统。这让补锅匠的生活变得更容易，你知道这意味着什么。[Tomas C]看到了一个机会，对他的小米大方 IP 相机进行改装，该相机被配置为只能与专有应用程序和云一起工作。

黑客通过拆开设备并在其上安装定制固件来取消保修。[Tomas C]发布的照片显示主板由一个 [Ingenic T20](http://www.ingenic.com/en/?product/id/14.html) 驱动，这是一个受欢迎的 IP 相机处理器，具有一些图像和视频处理子核心。成功刷新固件后，IP 摄像机现在可以进行多种操作，如远程录制和回放，可使用 web UI 进行配置，如[Tomas C]所述

我们对[定制固件](https://github.com/EliasKotlyar/Xiaomi-Dafang-Hacks)做了进一步的挖掘，发现定制固件的原作者【EliasKotlyar】在这个项目上做了很多工作。有大量的[拆相机的图片](https://github.com/EliasKotlyar/Xiaomi-Dafang-Hacks/blob/master/informations/teardown.md)和一组关于他如何入侵的优秀文件。从添加串行头，获得根访问，转储固件，甚至工具链链接的一切都在页面上给出。这对于想要进入游戏的新手来说非常方便。

IP 摄像头并不是唯一可以被黑客攻击的硬件。还有其他运行基于 Linux 的固件的设备，比如运行 OpenWRT 的 [Wifi SD 卡](https://hackaday.com/2016/06/30/transcend-wifi-sd-card-is-a-tiny-linux-server/)。如果你想开始你的下一个 IP 摄像头攻击，请查看[源代码中编译 OpenWRT 的基本指南](https://hackaday.com/2012/01/19/complete-guide-to-compiling-openwrt/)。

谢谢你的提示[Orlin82]