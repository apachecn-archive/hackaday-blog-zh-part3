# 把你的 RPi 3 变成 BLE 灯塔

> 原文：<https://hackaday.com/2016/03/27/turn-your-rpi-3-into-a-ble-beacon/>

随着树莓 Pi 3 的推出，蓝牙低能耗(BLE)现在由我们支配。在 BLE 中，有几种技术可以实现广播数据的单向信标。苹果从 2013 年开始推 iBeacon，谷歌去年刚刚推出了他们的 Eddystone 解决方案。

如果你想在你的 RPi 3 上瞄准谷歌的 Eddystone，[Yamir]已经帮你搞定了。他整理了一份关于在 Raspbian 内部建立 Eddystone-URL 信标的指南。这种类型的信标只是广播一个 URL。范围内的用户将收到通知，告知该 URL 可用，并且可以导航到该 URL。Eddystone-URL 在 iOS 和 Android 上都可以使用。

设置这个的过程非常简单。`hciconfig`和`hcitool`命令完成所有工作。[Yamir]甚至做了一个[计算器工具，为你自己的 URL 生成`hcitool`命令](http://yencarnacion.github.io/eddystone-url-calculator/)。虽然 is hack 很简单，但它是一个不错的五分钟项目。如果你的 Raspberry Pi 正在运行一个 web 服务器，作为一个更复杂的黑客的一部分，它也可以方便地广播你的 Raspberry Pi 的 URL。