# 双启动你的 Arduino

> 原文：<https://hackaday.com/2016/10/25/dual-boot-your-arduino/>

不久前，曾经有一段时间，所有酷孩子都在双启动他们的电脑:一边运行 Linux 进行黑客攻击，另一边运行 Windows 进行游戏。我们知道，我们在那里。但是为什么你会想要双启动一个 Arduino 呢？我们仍然对这个应用程序摸不着头脑，但是当我们看到一个很酷的黑客时，我们就知道了；[Vinod]将微小的表面贴装 EEPROM 焊接在已经很小的 AVR 芯片上！(查看下面的视频。)

除了微小的焊接技术，Vinod 还为基于 AVR 的 Arduino 编写了自己的引导程序。只要有足够的内存来备份 AVR 的闪存，引导加载程序就可以在闪存新程序的同时将现有程序转移到 EEPROM。更多详情，[阅读来源](https://github.com/vinodstanur/arduino_dualboot_bootlaoder)。

虽然您可能认为编写引导程序很难(it *can* be)，但是[Vinod]的简单引导程序应用程序是用 C 语言编写的，使用的风格应该是任何使用过 Arduino 的人都熟悉的。它当然可以针对大小进行优化，但可能不是为了可读性(和可调整性)。

你为什么想要双启动一个 Arduino？也许能够在同一台设备上运行测试和稳定的代码？你可以用 ESP8266 通过 WiFi 做同样的事情[。但是可能你没有 WiFi 可用？无论如何，我们喜欢黑客，因为“你可以”是一个足够好的借口。如果你真的有这样的想法，请在评论中发表吧！](http://hackaday.com/2014/11/13/programming-an-arduino-over-wifi-with-the-esp8266/)

 [https://www.youtube.com/embed/l3UTkA91U2k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/l3UTkA91U2k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

