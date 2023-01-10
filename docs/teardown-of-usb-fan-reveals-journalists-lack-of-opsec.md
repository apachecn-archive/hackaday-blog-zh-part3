# 拆除 USB 风扇暴露记者缺乏 Opsec

> 原文：<https://hackaday.com/2018/07/11/teardown-of-usb-fan-reveals-journalists-lack-of-opsec/>

上个月，新加坡主办了朝鲜和美国领导人峰会。受邀参加此次活动的注册记者获得了一个新闻资料袋，其中包括一瓶水、各种纸制品、[和一个插入 USB 端口的风扇](https://twitter.com/HaraldDoornbos/status/1005746788303867905)。

可以理解的是，Twitter 上的计算机安全人群笑得很开心。你不应该将随机的 USB 设备插入计算机，尤其是如果你是一名记者，尤其是如果你在国外，尤其是如果你正在报道近年来最引人注目的国际峰会。这样做是鲁莽的。

这不是一个关于 USB 风扇的故事，也不是一个关于拆卸风扇的故事，也不是一个关于世界各地的间谍机构侵入记者电脑的故事。这是一个需要更高意识的故事，关于我们把什么插入我们的计算机。在这种情况下，没有什么结果——大多数 USB 设备仅仅是这样，仅此而已。[其中一个风扇最近被拆了](http://www.cl.cam.ac.uk/~sps32/usb_fan_report.pdf) (PDF)数据线甚至都没连上。(我将在本文后面深入探讨这一点)。但这个轶事提供了一个谈论 USB 安全性的机会，以及如何首先通过几秒钟的深思熟虑来打断将每个 USB 设备插入计算机的冲动。

### 将随机设备插入您的计算机会出什么问题

为什么你不应该把一个随机的 USB 设备插入你的电脑的最好例子是 [Stuxnet](https://krebsonsecurity.com/2010/09/stuxnet-worm-far-more-sophisticated-than-previously-thought/) 。这种蠕虫病毒于 2010 年被发现，专门用于破坏伊朗的核离心机，其效果是摧毁伊朗五分之一的铀浓缩能力，并感染了数十万台计算机。

虽然自 Stuxnet 蠕虫病毒部署以来已经过去了大约十年，但它仍然是有史以来最令人印象深刻的网络武器。Stuxnet 利用 4 次 0-day 漏洞攻击专门针对核离心机的可编程逻辑控制器，逐渐提高和降低运行速度，直到一千台这些机器被摧毁。无论是谁编写了 stu xnet——目前最有可能的猜测是美国和以色列情报机构之间的合作——都对 Windows 漏洞和这些离心机上发现的西门子可编程逻辑控制器软件有深刻的了解。虽然 Stuxnet 相当复杂，但它最初是使用明显的低技术手段部署的。

Stuxnet 最初是通过一个 u 盘进入伊朗核设施的。确切的细节不得而知，但所有迹象都表明有人在不考虑后果的情况下将不受信任的设备插入计算机。

### USB 漏洞:常见的疑点

那么，使用随机 USB 设备的攻击看起来像什么呢？几年来，出现了几种不同的方法，它们都很吸引人。

用 USB 设备进入计算机的最好也是最容易的方法是击键注入攻击。这最好用一个 USB 橡皮鸭来完成，这是一个看起来像 USB 拇指驱动器的小装置。USB 橡皮鸭不是存储设备，而是包含一个模拟普通 USB 键盘的微控制器，并将击键有效载荷自动发送到计算机。例如，如果你在 Windows 电脑上，按 Alt+F4 组合键将关闭当前窗口。如果你给一个 USB 橡皮鸭编程，让它在插上电源时发出“Alt-F4”组合键，这个 USB 橡皮鸭就会关闭当前聚焦的窗口。

这些利用可以扩展。用更复杂的脚本给 USB 橡皮鸭编程可能会改变计算机的主机文件。每当用户在浏览器的地址栏输入 google.com，电脑就会调出 goggle.com。软件有效载荷可以通过命令行下载，安装键盘记录器。通过击键注入攻击，密码可以在几秒钟内被窃取。

这类攻击属于 BadUSB 攻击，[这是 2014 年](https://hackaday.com/2014/10/05/badusb-means-were-all-screwed/)首次讨论的内容。它不仅仅是一个 USB 橡皮鸭:普通的拇指驱动器可以被重新编程来执行击键注入攻击，而[一个一美元的微控制器](http://0xdeadcode.se/archives/581)可以被编程来执行相同的攻击。

关于实现，这种攻击唯一需要的组件是一个小的微控制器和一些无源组件。该微控制器将通过每个 USB 端口中的 D+和 D-线连接到计算机。给定一个(物理上)足够小的微控制器，USB 间谍设备看起来就像一个 USB 供电的风扇。区别的唯一方法是把它拆开，看看电路板。

[![](img/ef617dc348f77040529a0b83b15355f1.png)](https://hackaday.com/wp-content/uploads/2018/07/btkpnlzcaaapmop.jpg)

TURNIPSCHOOL, a device that becomes a wireless USB keyboard. Source: [Michael Ossmann](https://twitter.com/michaelossmann/status/491641360739352577)

除了 USB ducky 之外，通过 USB 设备进行的攻击还可能采取 COTTONMOUTH 的形式，这是一种由美国国家安全局创建的设备，并在 2013 年通过美国国家安全局的 ANT 目录泄露给了世界。 [TURNIPSCHOOL](http://www.nsaplayset.org/turnipschool) 是由 Great Scott Gadgets 开发并在 Shmoocon 2015 上展示的 COTTONMOUTH 的“克隆”。这种小电路板适合 USB 设备的塑料插头。这个小电路板可以在远程控制下成为一个定制的 USB 设备。你可以把它想象成一个无线 USB 键盘。

但是 USB 攻击不仅限于将 USB 风扇变成 USB 键盘。[USB ee 攻击](https://cyber.bgu.ac.il//t/USBee.pdf)将 USB 连接器上的数据总线变成天线，允许通过无线电进行数据渗透。如果你是一名向记者分发 USB 设备的国家级演员，并且你想要一些 lulz， [USB 黑仔](https://hackaday.com/2015/10/10/the-usb-killer-version-2-0/)是一个很好的选择；这只会烧坏任何计算机的 USB 端口(可能更多)。

简而言之，USB 设备有几十种有害的方式。不过，它们都有一个共同点:它们都使用微控制器，或者显然是复杂的电子设备。它们都将通过 USB 端口连接到 D+和 D-或 TX 和 RX 线路。了解了这一点，我们就可以定义一个威胁模型，描述通过随机 USB 设备进行攻击的情况。我们也知道如何测试这种威胁:如果 USB 端口中的 D+和 D-线之间有一些可测量的电阻(在几百千欧姆到几兆欧姆之间)，那么*可能有*存在。

### USB 风扇的分析结果

感谢《经济学人》的记者，剑桥大学的 Sergei Skorobogatov 分析了在 T2 峰会上分发的一个 USB 风扇。分析的第一步是探测 USB 端口的 D+和 D-线。这些连接是每个 USB 设备与计算机之间传输数据的方式。如果这些线路断开，就无法向计算机传输数据。分析的第一步发现了 1 千兆欧姆以上的电阻，表明它们与其他一切都断开了。由于这是一个 USB-C 连接器，TX1 和 TX2 数据线也被探测，发现它们也与其他任何东西断开。

[![](img/e46084426b7a8f570d5e0e172833f70d.png)](https://hackaday.com/wp-content/uploads/2018/07/guts1.png)

The USB-C connector and components of the Singapore fan

【Skorobogatov】对电路板的目测发现 VCONN 通过一个电阻连接到 VBUS。电路板上有两个二极管，可能是为了降低电动机的电压。在新加坡发布会上分发的这个特殊的 USB 风扇内部没有复杂的电子设备。这个装置是干净的，但只有在仔细检查后才能确定。

应该注意的是，USB 端口中 D-线和 D+线之间的电阻不是任何间谍软件、恶意软件或其他间谍设备的证据。连接到 USB 端口[数据线的电阻用于 USB 充电器](https://learn.adafruit.com/minty-boost/process)的设备协商。如果这款 USB 风扇的设计者想要从 USB 端口获得超过 500 mA 的电流(不太可能，但让我们来看看)，他们必须在数据线上安装电阻。因此，对任何 USB 的完整分析必须包括对电路板的目视检查。

### 为什么这很重要

通过在 Twitter 上发布 USB 风扇驱动器的图像开始这整个混乱的记者是非常能干和有能力的。作为一名战地记者，他在 2011 年的埃及和利比亚内战期间面临着巨大的危险，这只是他报道任务中的两个例子。仅仅凭借这些经历，这位记者对人身安全有所了解。但是计算机安全更抽象，同样的本能更难应用。

这里的真实故事是，有成就的记者会对外国政府给他们的随机 USB 设备心存感激。种种迹象表明，这位记者确实把这个 USB 风扇插到了他的电脑上。但即使他走了安全路线，选择使用 USB 电池或数据线断开的电缆来抵御恶意软件，我敢肯定其他人没有采取预防措施。在新加坡峰会的 2500 名记者中，有些人无疑将这一威胁输入了他们的电脑。

在有能力的专业人员和计算机安全的最基本原则之间存在着巨大的理解鸿沟。所以，有机会的话就告诉大家:不要把你的密码告诉别人。不要重复使用密码。也不要随便把 USB 设备插到电脑里。