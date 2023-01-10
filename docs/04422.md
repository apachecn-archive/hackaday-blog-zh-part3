# 一款引人注目的 Raspberry Pi 智能音箱

> 原文：<https://hackaday.com/2016/12/21/an-eye-catching-raspberry-pi-smart-speaker/>

[curcuz]的 [BoomBeastic *mini*](https://hackaday.io/project/15672-boombeastic-mini) 是一款基于 Raspberry Pi 的智能互联扬声器。但是不要把它当成另一个媒体中心项目。他的博客文章更多的是关于设置容器软件、启用 OTA 更新等的操作指南，对于一些人来说是一个很好的学习项目。此外，设计相当优雅和漂亮。

硬件很简单。这是树莓派——他得到了使用 Pi2、Pi2+、Pi3 或 Pi0 的说明。由于 Pi 的音频能力有限，他使用 DAC 来驱动扬声器，[Adafruit i2s 3W D 类放大器突破 MAX98357A](https://learn.adafruit.com/adafruit-max98357-i2s-class-d-mono-amp/overview) 。该器件使用的 I2S 是内部集成电路声音——一种 3 线对等音频总线——不要与 I2C 混淆。为了一些基本的视觉反馈，他增加了一个带有 I2C 接口的 [8×8 LED 矩阵。一位发言人完成了 BoM。外壳的灵感来自 Pimoroni PiBow，这是一叠激光切割的中密度纤维板。机箱设计经历了四次迭代，但最终结果看起来非常完美。](https://learn.adafruit.com/adafruit-led-backpack/overview)

在软件方面，该项目使用了[mo pidy](https://www.mopidy.com/)——一种 Python 应用程序，可以在具有网络连接和音频输出的设备上的终端或后台运行。开箱即用，它是一个 MPD 和 HTTP 服务器。用于控制 Mopidy 的其他前端可以从扩展中安装，例如支持 Spotify、Soundcloud 和谷歌音乐。为了允许无线编程，[curcuz]正在使用 [resin.io](https://resin.io/) ，这有助于简化物理上难以触及的设备的管理。整个事情是集装箱使用 Docker。关于设置所有软件和库的附加说明发布在他的[博客帖子](https://resin.io/blog/the-making-of-boombeastic/)上，代码托管在 [GitHub](https://github.com/resin-io-projects/boombeastic) 上。

在他的清单上有几件“要做的事”会让这件事变得更加有趣。同步音频是一个:在一个多设备的环境中，有可能同步它们并再现相同的音频。另一个是为 LED 矩阵添加表情符号和均衡器显示模式。如果您有任何建议，请告诉[curcuz]。

 [https://www.youtube.com/embed/EnLgmW8kyis?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/EnLgmW8kyis?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

