# 微型主板上的 Windows 10

> 原文：<https://hackaday.com/2015/12/03/windows-10-on-a-tiny-board/>

在过去的几个月里，许多公司和设计师已经开始挑选最新的英特尔片上系统。英特尔总得想办法干掉 ARM 吧？[这些单板 x86 电脑中最新的是 Lattepanda](https://www.kickstarter.com/projects/139108638/lattepanda-a-45-win10-computer-for-everything) 。这是一块小小的主板，可以运行 5 年前的台式电脑可以运行的一切，包括完整版的 Windows 10。

这不是我们最近几个月第一次看到微型 x86 主板了。去年 10 月，[一款借鉴了 Raspberry Pi 2 设计灵感的 x86 主板在 Kickstarter 上发布](http://hackaday.com/2015/10/18/an-intel-atom-cpu-in-the-raspi-form-factor/)。这些都是合适的个人电脑，能够运行 Windows 10、Linux 和世界上几乎所有其他环境。

Lattepanda 的规格包括运行速度为 1.8GHz 的四核 Cherry Trail 根据配置分为 2GB 或 4GB，以及 32GB 的 eMMC 闪存。外设包括 USB 3.0、以太网、WiFi、蓝牙和支持 HDMI 或 DSI 连接器的集成显卡。

但电脑当然只是电脑，你不能把只运行 Skype 的机器卖给‘创客’市场。Lattepanda 还包括一个 ATMega32u4 作为协处理器，为该板提供“Arduino 功能”。在我的日子里，我们走上两个方向，以获得一个并行端口，但我跑题了。

虽然这些微型 x86 主板可能不会在一年后上市，它们背后的公司可能会从地球上消失，但这些设备的引入预示着一场大战即将到来。英特尔想要低功耗 SoC 市场，这是一个迄今为止完全为基于 ARM 的设备保留的空间。