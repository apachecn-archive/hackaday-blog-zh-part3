# 用现代控制拯救旧洗衣机

> 原文：<https://hackaday.com/2018/01/02/rescue-an-old-washing-machine-with-modern-controls/>

不起眼的洗衣机是我们中很少有人真正热爱的电器。他们被期望进入我们的生活，忠实地服务，尽量不大惊小怪。在过去的好时光里，洗衣机使用 20 年以上是很常见的，这样做是为了讨好它的主人。可悲的是，虽然简单的机械部件可能仍然可以使用，但幕后的电子设备可能会出现故障。这是一个关于给老朋友一个新大脑的俄罗斯故事。

这个问题中的机器被称为黄鹂，已经服务了很长时间。逻辑芯片和整个控制器都被更换了，但仍不断出现故障。取而代之的是设计一种替代品来保持机器运行一段时间。为了简单起见，我们决定删除某些东西，而不是依赖于重新创建机器的完整功能集。消除了不同织物类型或洗涤模式的设置，如果像大多数人一样，所有洗涤都在同一模式下进行，这是一个简单的选择。发现水位传感器不再正常工作，并且消除比修理简单。

大脑是一个 PIC 微控制器，一个 ESP12 充当监视和控制的网络服务器。此外，从一些以前的医疗设备中取出一个玻璃透镜，整齐地安装在有机发光二极管显示器前的机器控制面板上，使机器获得比以前多得多的反馈。控制仍由机器的原始按钮完成。还增加了温度传感器，以便机器在出现过热问题时自动关闭。这一切都是绑在一起，看起来是一个经典的单面自制 PCB。

这是一个伟大的项目，它表明将现代电子力量运用到老式机械硬件上是很容易的，而且效果很好。一台洗衣机可以活到下一天，下一批货——而垃圾填埋场仍然会轻得多。

我们以前也看到过为旧洗衣机构建控制器——[比如用 Arduino 取代机械控制。](https://hackaday.com/2014/10/14/new-brain-for-an-old-washing-machine/)

【感谢泰洛特龙发来此文！]

 [https://www.youtube.com/embed/hqxMUa52ZLc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/hqxMUa52ZLc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

