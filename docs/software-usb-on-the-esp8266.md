# ESP8266 上的软件 USB

> 原文：<https://hackaday.com/2016/09/03/software-usb-on-the-esp8266/>

不久前，[cnlohr]需要一个 USB 键盘和鼠标。他的 box 'o junk 没有这个特殊的宝藏，他没有像普通的极客一样在亚马逊上跳来跳去，也没有像普通人一样*【cnlohr】决定将 ESP8266 变成一个 USB 键盘和鼠标。会有多难呢？ESP 不支持 USB，但是 bitbanging 之前并没有阻止他。[最终结果是一个运行在 ESP8266 WiFI 模块](https://www.youtube.com/watch?v=FPBzOaLbWhM)上的 USB 堆栈。*

 *[cnlohr]已经为 ESP 的 USB 实现工作了大约一个月，从逻辑分析器、Wireshark、Xtensa 汇编和大量迭代开始。这种硬件黑客的最终结果是一个基于 ESP8285 的电路板，这是一个集成闪存的 8286，可以紧密地安装在 USB 插座中。

这种微型板模拟低速 USB (1.5 Mbps)，对于存储、串行或 USB 做的任何更好的事情来说都不够快，但对于键盘和鼠标来说已经足够好了。现在，[cnlohr]的 ESP USB 设备正在托管一个网页，通过将该网页加载到他的手机上，他在手持触摸屏上拥有了一个虚拟键盘和鼠标。

如果你一直在关注的话，[cnlohr]现在已经将[以太网](http://hackaday.com/2016/04/01/ethernet-controller-discovered-in-the-esp8266/)和 USB 带到了一个微小的微控制器上，可以通过通常的在线商店花几美元买到。如果你想建立自己的 ESP 盘，所有的文件[都在 Gits](https://github.com/cnlohr/espusb) 上。

谢谢你的提示。

 [https://www.youtube.com/embed/FPBzOaLbWhM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/FPBzOaLbWhM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

*