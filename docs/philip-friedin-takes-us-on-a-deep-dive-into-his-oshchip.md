# 菲利普·弗里丁带领我们深入了解他的 OSHChip

> 原文：<https://hackaday.com/2016/03/08/philip-friedin-takes-us-on-a-deep-dive-into-his-oshchip/>

每月一次，海湾地区的黑客和工程师夜间聚集在我们邪恶霸主(Supplyframe)的大办公室，带我们进行一次硬件冒险。在过去的一个月里，[Philip Friedin]带我们亲自参观了 Osh chip，这是一个我们在去年的页面上看到的 T2 项目。OSHChip 可能看起来像另一个开源开发板，但 DIP 包和所有打包的功能都表明 OSHChip 是一个经验丰富的双 e 的后代。

[菲利普]给了我们一些额外的调整，使 OSHChip 成为一个具有许多功能的生物。对于大脑，它有一个运行在 Nordic nRF51822 内部的 16 MHz ARM Cortex-M0。虽然 16 MHz 不会让你在全球芯片短跑奥林匹克中赢得第一名，但是这款芯片*确实*在其外围设备中提供了一些特殊的东西。虽然我们只有 14 个 I/O 引脚，但外设和引脚通过一个全交叉开关连接，这意味着*的任何*引脚都可以映射到*的任何*外设。这种芯片还具有“任务-事件”系统，其中外围事件可以触发独立于处理器的简单行为。最后，我们不会想到北欧没有忘记他们的无线硬件。该芯片还内置了蓝牙(BLE)无线电，无需任何额外的硬件就能让您的无线项目充满活力。

为其他开发板编程通常需要一些不情愿的承诺。无论是专有的 IDE 还是不熟悉的操作系统，我们通常都需要安装一些额外的绒毛来将代码加载到我们的微控制器上。但不是 OSHChip。【菲利普的】自定义编程器插上插头就伪装成 u 盘，编程就像把一个十六进制文件拖到你 PC 上的文件夹里一样简单。最后，由于它是一个 ARM 芯片，您可以使用任何您喜欢的开源 ARM 工具链来生成可执行文件。

最后，我们不能把视线从 OSHChip 移开，而不评论它是多么可爱！OSHChip 封装在经典 DIP-16 封装中，对于标准试验板上的原型来说非常方便。因此，它非常小——小到可以放进一个盒子里，也可以打开你的智能手表！

你可以称 OSHChip 为开发板，甚至是芯片冒名顶替者！在休息后的视频中，让[Philip]指导您如何使用这款小巧灵活的 DIP-16 beast。

 [https://www.youtube.com/embed/dCimvCcck7A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/dCimvCcck7A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

