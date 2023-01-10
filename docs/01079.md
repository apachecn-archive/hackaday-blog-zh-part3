# 又一个 Pi Zero USB 集线器

> 原文：<https://hackaday.com/2015/12/30/yet-another-pi-zero-usb-hub-2/>

树莓派 Zero 本周在 Adafruit 重新上架，上架时间约为 8 分钟。这意味着更多的人得到π0，更多的人将把它们放在易贝上，每个人都在开发自己版本的 USB 集线器。最新版本的 Pi Zero hub 来自[Nate]，他做得很好。[他的 Pi USB 适配器](https://hackaday.io/project/8984-one-more-raspberry-pi-zero-usb-hub)增加了四个 USB 端口和其他 DIY USB 集线器中没有的功能，如保险丝和 ESD 保护。

与其他 Pi Zero USB hub 插件一样，这个构建依赖于一个 USB hub 控制器、几个无源器件，没有其他什么。该集线器中使用的芯片是 FE1.1s 芯片，这是一种高度集成的 4 端口集线器控制器，可以通过通常的中国经销商找到。这个集线器控制器要求不多，只需要一个 12MHz 的晶体，几个无源，四个 USB 插孔。

特别令人感兴趣的是[Nate]如何将这个中枢连接到 Pi 零点。他选择使用 USB 电缆，或者直接在 Pi 和 hub 之间焊接 USB 差分对。在这两种情况下，中枢都应该工作，加上 zeners，保险丝和其他防止中枢自我烧毁的部件，[Nate]可能会有一个非常好的项目。