# DEF CON:在高清晰度中实现现代化

> 原文：<https://hackaday.com/2016/08/06/def-con-bsodomizing-in-high-definition/>

几年前，[金并]又名[乔·格兰德](2014 年黑客日奖的评委)设计了有史以来最漂亮的电子恶作剧。BSODomizer 是一款简单的设备，带有 VGA 显示器和红外接收器的直通连接。将测谎仪插入一位毫无防备的同事的显示器，按下遥控器上的一个按钮，就可以看到微软的蓝屏死机了。如果你选择正确的微控制器，它是一个聪明、狡猾、实际上相当简单的器件。

[原来的 b 减磨器](http://www.grandideastudio.com/bsodomizer/)在齿中变得有点长了。VGA 终于死了。用于生成视频的 Propeller 芯片只能生成文本，无法再现微软新奇的图形错误屏幕。HDMI 代表着未来，而 FPGAs 从未像现在这样容易获得。对于今年的 DEF CON，【金并】和【佐兹】需要*的东西*来打动刚刚学习如何焊接的观众。他们重访了 BSODomizer，并在今年的 DEF CON 上创造了最伟大的硬件项目。

在简单地决定将 HDMI 添加到原始的 BSODomizer 之前，[金并]和[佐兹]做了聪明的事情，并找出了这种新的，更新的显示恶作剧玩具的功能。全彩色 1080p 是必须的，图像应该可以从 SD 卡上下载，动画将是一个很酷的功能。该 SD 卡提供了一些可能性，因此他们也在考虑采用屏幕帽，赋予 BSODomizer HD pentesting 远远超出原始产品的功能。这些特性意味着需要 FPGA。

为 BSODomizer HD 原型选择的开发板是 Cyclone V GX 开发板，通常在零售商处购买，价格约为 170 美元。对此，该团队添加了来自 T2 模拟公司的 HDMI 收发器。之后只是学习 Verilog，FPGA 开发，把像素推到屏幕上。

创建一些测试模式后，下一步是通过 HDMI 电缆传输图像。一个 24bbp 的 1920×1080 的图像几乎是 6 兆字节，这意味着需要一些快速内存。该内存以 512 MB lpddr 2 的形式添加到项目中，对于长动画来说绰绰有余。添加一个小 PIC 微控制器来跟踪电池，并作为红外遥控的触发器，原型或多或少是完整的。

几周工作的结果是一个电路板的三明治，它太贵了，不能作为一个产品，太大了，不能作为一个 1337 笔测试设备，也没有有价值的屏幕捕捉功能。在 BSODomizer HD 上还有很多–*很多–*工程要做，但如果有足够的兴趣和需求，这可能会成为一个真正的产品。

为了与最近的 DEF CON 传统保持一致，这个项目更多的是对一种技术的介绍，在这种情况下是 HDMI 和可编程逻辑。在互联网上的其他地方，人们多年来一直在将更酷的 FPGA 和 HDMI 混搭在一起，包括在加密的 HDMI 流上覆盖视频的[，以及在将像素传递到 HDMI 输出端口之前查看像素的](http://hackaday.com/2012/01/21/overlaying-video-on-encrypted-hdmi-connections/)[各种流光溢彩克隆](http://hackaday.com/2015/04/25/fpga-based-ambilight-clone/)。即使构建一个带 HDMI 输入和输出的 FPGA 解决方案也有点矫枉过正—[这个板](https://www.scarabhardware.com/minispartan6/)是一个带一堆 Verilog 的 BSODomizer HD 的完整解决方案。尽管如此，这个项目的原型是精致的，即使演示对房间里的孩子来说并不完全安全。

看看这个原始 b 减反射器的视频。

 [https://www.youtube.com/embed/EtNZjXMae1U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/EtNZjXMae1U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

