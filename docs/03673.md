# Raspberry Pi 为您的汽车添加了数字仪表板

> 原文：<https://hackaday.com/2016/09/28/raspberry-pi-adds-a-digital-dash-to-your-car/>

想办法让你的旧车变得更高科技吗？为什么不加一个花哨的数字显示器呢？来自[Greg Matthews]的这个黑客就是这样做的，使用树莓 Pi、 ~~OBD-II~~ 咨询阅读器和液晶显示屏[创建一个数字仪表盘，可以在你的老式模拟表盘旁边(或前面)运行](https://www.youtube.com/watch?v=5C9ypE6JUuY)。

[Greg 的] hack 使用了一个 [Raspberry Pi Foundation 显示器](https://www.adafruit.com/products/2718)，它包括一个触摸屏，所以你不需要鼠标或其他控制。Node.js 通过使用 Chromium 显示的网页显示速度、RPM 和发动机温度(检查发动机灯和其他警告是计划增加的)。节点页面正在从 Pi 上另一个监控 ~~CAN~~ 咨询总线的程序中获取信息。将它用于更具未来感的显示器会很有意思，比如微型投影仪和用于平视显示器的单向镜。

为了给系统供电，[Greg]使用了一个 [Mausberry 电源](http://mausberry-circuits.myshopify.com/collections/car-power-supply-switches/products/3a-car-supply-switch)，它从你的汽车电池中获取电力，但当点火关闭时，它也会干净地关闭 Pi，因此它不会耗尽你的电池。当你把一个来自易贝的 ~~OBD-II~~ 咨询阅读器和[咨询仪表板](https://github.com/gregsqueeb/consultDash)软件(Greg)写来解释和显示来自 ~~OBD-II~~ 咨询总线的数据，你会得到一个体面的数字仪表板显示。当然，这不是特斯拉触摸屏，但 170 美元，便宜得多。花更多的钱，你就可以轻松地把 60 英寸的手机从你的客厅搬到你的笔记本里，并且仍然可以使用树莓派。

你会在这个系统中加入什么样的额外功能？你的速度游戏化？长期燃油平均？请在评论中告诉我们。

**更新**——这篇文章最初将这次黑客攻击列为从 OBD-II 总线上进行。不过这款车没有 OBD-II，而是使用日产使用的较老的数据总线 Consult。对于任何困惑，我深表歉意！

 [https://www.youtube.com/embed/5C9ypE6JUuY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/5C9ypE6JUuY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

