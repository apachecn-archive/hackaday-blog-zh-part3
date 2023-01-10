# 廉价的 Powerbank 逻辑和拆卸

> 原文：<https://hackaday.com/2016/12/21/cheap-powerbank-logic-and-teardown/>

许多英国大街上都有英镑商店。无论你在世界的哪个角落读到这篇文章，你都可能有一个对等的版本；所有出售的商品价格都一样低的商店。他们可能被称为一元店，一欧元店，或类似的商店。在这种情况下，一英镑，今天翻译成 1.24 美元以下的阴影。

在略显随意的杂货和家用产品中，有一小部分是电子产品。调频收音机、USB 电缆和集线器、耳机和手机配件。其中一个引起了朱利安·伊雷特的注意，那就是 USB 电源库。(视频嵌入下方。)

一英镑买不到多少东西，这一点在这款产品中有所体现。一根在最小电流下就会变热的 USB 电缆，一个声称 1200 毫安时容量的 5V 输出 800 毫安，所有这些都来自一个来源不明的 18650 锂离子电池。有源元件是一个 [FM9833E SOIC-8 开关稳压器和充电器](http://www.superchip.cn/Private/ProductFiles/FM9833（移动电源专用管理 IC）.pdf) (220K PDF 数据手册，中文)。

一件近乎垃圾的消费电子产品的简单拆卸通常不会被视为我们会诱惑你的事情，但[朱利安]继续用这些设备进行一些毫无意义但有趣的娱乐。如果你把它们用菊花链连接起来，就可以显示出它们具有基本的数字逻辑特性，在我们放在断点下面的视频中，他要演示的就是这个。我们看到一个双稳态锁存器，一个置位复位锁存器，一个非常慢的非稳态多谐振荡器，最后他为环形振荡器拉出了一个负载更多的电源组。

如果[MacGyver]发现自己被困在某个只有解决一个复杂的数学难题才能让他解脱的地方，也许他可以制造出一台完整的计算机！最好的结论是[朱利安]自己在视频结尾给出的，他建议(我们在这里转述)如果你觉得这个想法不值得，你可以在评论中告诉他。

 [https://www.youtube.com/embed/Roxa2NjHz3M?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Roxa2NjHz3M?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



你能以如此低的价格在一个产品中买到所有这些是一个小小的奇迹，所以正如你所料，这并不是我们社区中的人第一次将注意力转向一元店商品。我们给你带来了[一元店蓝牙相机触发器，泄露了它的秘密](http://hackaday.com/2016/09/14/hacking-a-dollar-store-bluetooth-device/)，还有一个[计步器变成了电压表](http://hackaday.com/2012/11/12/4-volt-meter-from-a-dollar-store-pedometer/)。请继续关注，肯定会有更多的设备以低廉的价格登上货架。

我们以前报道过[朱利安]，当时[他发现了一种非常便宜而且非常亮的 LED 阵列](http://hackaday.com/2014/03/05/monster-100w-led-flashlight-for-under-10/)。