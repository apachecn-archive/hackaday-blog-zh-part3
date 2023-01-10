# Hackaday 解释道:Li-Fi &可见光通信

> 原文：<https://hackaday.com/2015/12/11/hackaday-explains-li-fi-visible-light-communications/>

一种新的数据传输方式即将出现，它可能会从根本上改变设备之间的对话方式:LiFi。LiFi 是 Light Fidelity 的缩写，它使用可见光发送数据，通过不可见的光脉冲在路由器和设备之间建立链接。这种可见光通信(VLC)使用了几乎每个房间都有的东西:LED 灯泡。

### 什么是生活

Li-Fi 听起来像是一个工程师狂热的梦想:它快速、廉价、安全且易于实现。高达 10Gbps 的速度已经在实验室中进行了演示，现在已经有提供 10Mbps 速度的 [产品](http://purelifi.com/lifi-products/li-flame/) 。它之所以便宜，是因为它可以使用 [一种经过改良的 LED 灯泡](http://hackaday.com/2015/09/27/sending-the-internet-from-an-led-lightbulb/) 。它是安全的，因为它只在光线可见的地方工作:走出房间，信号就会消失。它很容易实现，因为它使用了现有的技术:发光二极管。

这项技术的基础是快速打开和关闭 LED 灯。通过每秒开关 LED 数百万次，你可以创建一个传感器可以检测到的数据信号，但人眼是看不见的。在另一端，另一个 LED 检测到这些脉冲，并可以发送光脉冲作为响应，从而创建一个双向链接。如果你将它与有线以太网或 WiFi 网络结合起来，你会得到一个令人惊叹的组合:最后一个链接使用可见光的互联网连接。

 [https://www.youtube.com/embed/wVNXvjyxSYk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/wVNXvjyxSYk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



有一种方式可以把它想象成一个红外线遥控器，但却是用了类固醇。您的红外遥控器以大约 [38KHz 的频率打开和关闭红外 LED，以高达 120bps](https://en.wikipedia.org/wiki/RC-5) 的速度编码数据。电视中的传感器和微控制器检测到这种光，并将其转换为命令。20 世纪 90 年代的一些计算机和 PDA 使用了一种更快的标准，称为 [IrDA](http://www.irda.org/) ，可以以千比特的速度发送数据。然而，IrDA 从未真正流行起来，尽管它背后的团队正在开发新版本，可以将速度提升到 10Gbps。

Li-Fi 使用了与 IrDA 类似的想法，但用可见光代替了 IR。这具有电磁频谱更宽的优势，通过一些巧妙的编码，现代白色 led 的红色、绿色和蓝色元素可以用来增加可以发送的数据量，这种技术被称为色移键控(CSK)。因为数据是由 LED 光源发送的，所以也可以聚焦。字面意思:你可以用透镜来引导信号。

这项技术的支持者正计划利用房间天花板上的小型 LED 设备来构建网络，他们称之为 attocells。因为它们使用可见光，这些触角可以在非常小的(和聚焦的)角度上传输和接收，所以它们不会像 WiFi 设备那样相互干扰。在最近的一篇论文[](http://www.homepages.ed.ac.uk/hxh/Li-Fi_PAPERS/15_cheng_ecoc_invited.pdf)中，这项技术的支持者声称，在一个典型的 400 平方米的办公室中，这可以为设备提供 12 到 48Gbps 的速度:远远超过 WiFi 或其他必须处理其他类似设备干扰的无线网络。

另一个有趣的新进展是将 Li-Fi 信号与太阳能电池结合起来。通过一点巧妙的工程，太阳能电池既可以为一个小型设备供电，又可以接收 Li-Fi 信号。因此，设备可以从同一个来源接收电力和数据，这对于物联网设备或小型传感器非常有用。

### Li-Fi 有什么标准吗？

目前，Li-Fi 还没有真正的标准。当前可用的系统部分基于定义网络物理层的 IEEE 802.15.7 标准的 [，但是这已经相当过时了。然而，标准正在到来:Li-Fi 联盟是致力于创建类似 WiFi 的标准的主要团体，该标准将提供与 WiFi 设备相同的互操作性。不过，目前还没有时间表。](https://standards.ieee.org/findstds/standard/802.15.7-2011.html)

### 我如何能尝试 Li-Fi？

目前有两种方法:购买第一批设备，或者自己制造。PureLiFi 是第一家销售 LiFi 设备的公司:第一款 [第一款](http://purelifi.com/lifi-products/li-1st/) 。从那时起，该公司还增加了[lif lame](http://purelifi.com/lifi-products/li-flame/)，这是他们 attocell 概念的第一个版本。使用天花板上的设备和 USB 收发器，它可以以高达 10Gbps 的速度发送和接收数据。

另一种选择是自己做。迪士尼研究发表了一篇论文，展示了他们如何使用运行 Linux 的 Atheros SoC 板在现有的电灯插座 中构建一个 [类似 Li-Fi 的设备。不幸的是，他们没有公布任何原理图或代码。](http://www.disneyresearch.com/wp-content/uploads/Linux-Light-Bulbs-Enabling-Internet-Protocol-Connectivity-for-Light-Bulb-Networks-Paper.pdf) 

然而，Hackaday reader [jpiat]已经做到了:他的项目使用一个 [Arduino 来控制一个 RGB LED 灯，使用一个经过修改的 1 瓦 LED 灯](https://github.com/jpiat/arduino/wiki/Arduino-simple-Visible-Light-Communication) 来发送数据。他的系统只在一个方向上工作，但非常简单:Arduino 对数据使用简单的编码，并用三条数据线来控制 LED。不过，它足够强大，可以以相当快的速度发送:他声称，使用 1 瓦的 LED 灯，它可以在 3 米的距离内达到令人印象深刻的 1kbps 的速度。这是我们未来生活的精彩一瞥。

![The home-made VLC system built by [jpiat]](img/b949f6cf7e06b1e0b02372a11fd92d04.png)

The home-made VLC system built by [jpiat]