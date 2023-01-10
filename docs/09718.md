# Chromebook 用相机换取 WiFi 自由

> 原文：<https://hackaday.com/2018/06/13/chromebook-trades-camera-for-wi-fi-freedom/>

现在有许多公司提供满足自由软件基金会“尊重你的自由”认证标准的交钥匙计算机。这意味着，在一般意义上，计算机保证不会监视你或者做任何你没有明确要求它做的事情。不幸的是，这些机器往往有一个巨大的溢价附加，使它成为隐私和性能之间的一个令人不快的决定。

热爱自由的黑客[SolidHal]写信告诉我们他寻求在不倾家荡产的情况下创造一款符合 FSF 标准的笔记本电脑。基于廉价的华硕 C201 Chromebook，他的定制机器检查了所有合适的框。安装 Debian 后，操作系统变得非常简单，引导加载程序也摆脱了任何英特尔管理引擎的恶作剧，只需要一剂健康的 Libreboot。但有一个问题:永久安装的 WiFi 硬件需要专有固件。为了解决这个问题，他决定[安装一个内置 USB Wi-Fi 适配器，这个适配器有 FSF](https://github.com/SolidHal/AsusC201-usb-wifi-from-webcam)的认证印章。

由于 Chromebook 显然没有内部 USB 端口，这说起来容易做起来难。但由于[SolidHal]不是那种首先会希望自己的笔记本电脑为他拍照的人，他想到了利用集成网络摄像头使用的内部 USB 连接。他拔出网络摄像头，研究布线，并确定哪些线对应于正常的 USB 引脚。

他选择的 FSF 认可的 ThinkPenguin Wi-Fi 适配器非常小，因此可以很容易地将其塞进 Chromebook 内部的一些空白空间。[SolidHal]只需要将它焊接到旧的网络摄像头连接上，并用 Kapton 胶带包裹起来，以防止任何可能的短路。考虑到天线和所有嘈杂的组件都卡在机器内部，信号可能不是很好，但这是拥有完全免费和开源驱动程序的一个权衡。但是正如已经确定的那样，当[沿着圣伊努西乌斯正义的脚步前行时，有时你不得不做出艰难的选择。](http://hackaday.com/2017/12/13/accident-forgiveness-comes-to-gplv2/)

像这样的笔记本电脑内部改造让我们想起了过去的黑客时代，[那时 Eee PC 改造风靡一时](https://hackaday.com/2008/01/19/add-everything-to-your-eeepc/)，我们仍然在屏幕上“粘贴”黑白图片。啊，回忆。