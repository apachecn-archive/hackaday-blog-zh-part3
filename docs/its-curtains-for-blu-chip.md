# 这是蓝光芯片的窗帘

> 原文：<https://hackaday.com/2017/12/12/its-curtains-for-blu-chip/>

理论上，没有理由你不能在你的房子里实现自动化。然而——除非你独自生活——你需要考虑到大多数人不会接受你挂在到处都是的试验板上的看起来杂乱无章的电路。现在照明变得很容易，因为有很多商业选择。然而，仍然有很多事情需要自动化。对[jeevanAnga]来说，窗帘迫切需要遥控。

由于手机无处不在，将手机用作控制器是有意义的，蓝牙低能耗(BLE)非常适合这种应用。但是你不能把一大堆难看的电线挂在窗帘杆上。这就是为什么[jeevanAnga]使用一个微小的(16.6 x 11.5 毫米) [BLE 董事会称为 BluChip](http://www.instructables.com/id/Automated-Home-Curtains-BluChip/) 。

我们没有验证它，但[jeevanAnga]声称这是最小的 BLE 板，它肯定很小。你可以在下面的视频中看到结果。

当然，BluChip 只对着电话说话。步进电机在皮带、滑轮和齿轮的帮助下完成繁重的工作。BluChip 还需要一个独立的程序员，这并不是很小，但是当然，你只在配置设备时需要它。

在内部，BluChip 是一个 ARM 处理器(带 256K 闪存和 32K RAM 的 Cortex M0)。它的工作电压为 1.8 到 3.6 伏，并且通过了 FCC 认证，所以你可以很容易地在商业产品中使用它。大多数有用的信号被带到 0.1 英寸中心的引脚上，这很方便。

你仍然需要一点支持硬件(如步进驱动器)，所以挑战是使设备足够有吸引力，可以放在客厅里。好消息是，你几乎可以把那块小小的 BLE 板偷偷带到任何地方。

如果你想要一本关于 BLE 的入门书，你可以阅读基础知识。我们也看到过非 BLE 的主板[被黑客攻击来使用协议](https://hackaday.com/2013/09/21/sending-data-over-bluetooth-low-energy-with-a-cheap-nrf24l01-module/)。

 [https://www.youtube.com/embed/yTDoNZluRZk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/yTDoNZluRZk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

