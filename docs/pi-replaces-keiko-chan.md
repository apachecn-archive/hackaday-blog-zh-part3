# Pi 取代 Keiko-chan

> 原文：<https://hackaday.com/2017/11/30/pi-replaces-keiko-chan/>

[Tobias Kuhn]和他工作场所的一些同事构建了 [Crystal Signal Pi](https://hackaday.io/project/20060-crystal-signal-pi) ，这是一种基于 Raspberry Pi 的低成本通知设备，可以提供关于服务器问题的视觉、音频和网络警告。[Tobias]为一家[日本公司](https://www.infiniteloop.co.jp/)工作，在那里，服务器始终保持良好运行至关重要。任何紧急情况或错误情况必须立即广播，以便技术人员可以尽快修复。启用网络的警示灯杆用于提供这些警报。一家当地公司生产了一系列指示器和危险警示灯，俗称 [Keiko-chan](http://www.isa-j.co.jp/english/spec/index.html) 。这些灯类似于通常安装在工厂车间机器或多种车辆(如叉车)上的危险警告塔灯。Kieko-chans 增加了一些功能，使其更适合在服务器数据中心使用——一个用于有线网络的千兆位 LAN 端口和一个用于 WiFi 模块的 USB 端口。因此，除了视觉和听觉警告，它还可以通过网络传输信息，提醒维修人员。使用这种商业解决方案不应该是一个问题，如果不是他们每瓶将近 500 美元的高昂价格。

所以[托拜厄斯]决定围绕树莓派打造自己的警示灯。经过两轮原型设计，一个简单的帽子被设计出来，可以插入到 Pi 中。硬件的细节是粗略的，但它是足够简单的数字。零件清单包括一个 PLCC-6 风格的 RGB LED，三个晶体管来驱动三个 LED 引脚，一个稳压器，一对电解电容和一个大按钮。一个简单的丙烯酸外壳和一个安装在 RGB LED 顶部的丙烯酸圆柱体为指示器创造了一个漂亮的边缘照明效果。

Crystal Pi 的代码托管在 Github 上，并且包含了方便的脚本来简化安装。一旦安装完毕，可以通过基于 web 的 GUI 或 API 访问和控制 Crystal Pi。还有一些更有趣的特性已经实现或计划在以后实现，所以请查看博客和资源库了解更多。看看下面的视频，看看运行中的水晶 Pi。

 [https://www.youtube.com/embed/BJKb3eEmUsY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/BJKb3eEmUsY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

