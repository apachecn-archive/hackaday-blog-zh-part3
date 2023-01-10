# 用于高质量 RF 信号的微型树莓 Pi 屏蔽

> 原文：<https://hackaday.com/2016/03/16/tiny-raspberry-pi-shield-for-high-quality-rf-signals/>

在它的许多技巧中，Raspberry Pi 能够在其 GPIO 引脚上输出时钟信号，这被证明是在业余无线电波段合成 RF 信号的最佳选择。然而，[Zoltan]意识到产生的信号相当脏，所以他想出了一个聪明的 Pi 屏蔽来调节 RF 信号，将 Pi 变成高质量的低功耗发射机。

[Zoltan]在一个小屏蔽中塞进了一个用于宽带噪声的带通滤波器，一个用于谐波的低通滤波器，以及一个用于稍微增强信号的功率放大器，这个小屏蔽被巧妙地设计成适合任何版本的 Pi。即使有了功率放大器，最终的发射机仍然正好处于 [QRP](http://hackaday.com/2016/03/08/how-low-can-you-go-the-world-of-qrp-operation/) 的范围内，并且屏蔽层被优化用作 20 米波段上的 [WSPR](http://hackaday.com/2013/03/21/wspr-transmitter-shows-true-value-of-raspberry-pi-for-hacking/) 信标。但是[有大量的 Pi 软件](https://github.com/F5OEO/rpitx)可以让火腿尝试其他模式，包括 CW、FM、SSB，甚至 SSTV，以及其他用于不同波段的[信号调节硬件](http://shop.languagespy.com/collections/frontpage/products/pi-tx-transmitter-kit-for-the-raspberry-pi)。

是的，这些都是市场上可以买到的产品，但是即使你不在市场上购买这样的盾牌，或者如果你想推出自己的盾牌，从[Zoltan]在 2015 年 TAPR 数字通信大会上的演讲中也有很多东西可以学习。他讨论了在获得与每种 Pi 版本兼容的薄型屏蔽时遇到的困难，以及导致决定使用 SMT 元件的设计限制。

 [https://www.youtube.com/embed/w-OTpw2Ai0k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/w-OTpw2Ai0k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

