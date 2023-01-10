# KiCad 第 5 版有什么新内容

> 原文：<https://hackaday.com/2018/02/10/whats-coming-in-kicad-version-5/>

至少在五年前，如果你想设计一个印刷电路板，最好的选择是 Eagle。现在，Eagle 是 Autodesk 的财产，许可模式已经改变(尽管*仍然有*免费版本，人们)并且开源 EDA 套件 KiCad 变得越来越好。新的开发者正在为这个项目做出贡献，从某些方面来看，KiCad 现在是开发开源硬件最流行的工具。

在上周的 FOSDEM 上，KiCad 的项目负责人[Wayne Stambaugh]展示了即将发布的版本 5 中会有哪些特性。KiCad 只是不断改进，这些新功能真的是杀手级的功能，会让每个(不公正地)对 Eagle 的新授权感到恼火的人非常高兴。

尽管 KiCad 的最新版本对零件和封装外形库的处理方式进行了改进，但即将到来的重大变化是封装外形库将安装在本地。用于图书馆管理的 Github 插件——理论上是个好主意——不再是默认的。Spice 模拟也即将来到 KiCad。即将到来的 Spice 集成的最佳演示是[这个相对较老的视频](https://www.youtube.com/watch?v=2WDPzW6DGzQ)演示了 KiCad 如何将原理图转化为电压和电流的图形。

然而，最大的新闻是导入 Eagle 项目的新功能。[Wayne]在舞台上现场演示了这一点，他导入了一个 Eagle 板和 Arduino Mega 的原理图，并在几秒钟内将其转换为 KiCad 板和原理图。它还不太完美，但已经很接近了，而且非常非常好。

当然，还有其他一些奇特的特性可以让原理图和 PCB 的设计变得更加容易。Eeschema 正在获得一个更好的配置对话框，改进的总线和电线拖动，以及改进的连接处理。Pcbnew 支持圆角矩形和复杂焊盘形状，直接导出到 STEP 文件，您很快就可以从原理图更新电路板，而无需更新网表文件。慢慢地再读一遍最后一个特写。这是我们听到的最好的消息。

此外，这是你能听到韦恩讲话的难得机会之一。这意味着关于 KiCad 发音的争论结束了。是' *Key-CAD* ，不是' *Kai-CAD* 。你可以在下面查看[韦恩]关于 KiCad 的*状态的全部内容。*

 [https://www.youtube.com/embed/xhcD9zJufLA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/xhcD9zJufLA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

