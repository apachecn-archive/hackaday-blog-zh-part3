# 由新驱动程序带来的退休的翻转点显示

> 原文：<https://hackaday.com/2017/11/21/flip-dot-display-brought-out-of-retirement-by-new-drivers/>

LED 矩阵显示器和平板显示器已经在很大程度上取代了用于公共标牌的老式机电型号。我们认为这是一种耻辱，但对修补者来说这也是一个福音，因为如今在网上市场上可以买到廉价的旧显示器。

约翰·惠汀顿和他从一辆旧公共汽车上抢救出来的翻转点显示器就是如此。他想让旧标志恢复工作，但是没有一个像样的司机，他做了一个在这种情况下会做的事情——他把它拆下来，逆向工程。像大多数这样的显示器一样，他的汉诺威显示器 7 x 56 像素翻转点标志在机电方面很有趣；每个像素是一张卡片，横跨在一个小电磁铁的两极上。脉冲磁铁和卡片翻转，改变像素从黑色到荧光绿色。[John]使用现有的标牌驱动程序和逻辑分析仪来确定内部电子设备驱动像素所使用的协议，并提出了一种改进很多的发送字符和图形的方法。随着树莓 Pi 和电源现在驻留在外壳内，基于网络的 GUI 让他可以轻松地显示信息。下面的视频有很多细节，[代码是免费的](https://github.com/tuna-f1sh/node-flipdot)。

你可能会想起[中的【约翰】最近的一次侧光谢妮式展示](http://hackaday.com/2016/12/22/light-pipes-and-leds-team-up-for-a-modern-take-on-the-nixie-tube/)。看起来他对引人注目的展示情有独钟，我们对此没意见。

 [https://www.youtube.com/embed/HoeJRwjy5dY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/HoeJRwjy5dY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

