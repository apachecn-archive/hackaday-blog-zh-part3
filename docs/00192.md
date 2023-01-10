# STM32 JavaScript 偷看和戳

> 原文：<https://hackaday.com/2015/09/25/stm32-javascript-peeks-and-pokes/>

许多人发现脚本语言非常高效，我们已经看到相当多的芯片现在支持你通常认为的脚本语言。这些高级抽象语言是伟大的，直到他们不是。当你需要深入抽象，做一些复杂的事情，或者你需要每一个性能周期，你可能不得不打破你的常规工具。

Espruino 是一款内置 JavaScript 的 ARM 处理器(一款 STM32)。然而，[Gordon Williams]展示了如何在需要时使用 peeks 和 pokes 直接访问硬件。这些名字来源于另一个流行的抽象的出口。旧的 BASIC 语言允许使用关键字 peek 和 poke 进行直接内存访问。[Gordon]展示了一些访问 PWM 定时器的示例，甚至查看了 STM32 参考手册，以说明他如何知道从哪里开始查看和查看。

我们不喜欢你不能打破的抽象层。如果 C 不能嵌入或调用 assembly，它就不会像现在这样强大。给高级用户一个打破抽象的方法，让它在更多的情况下更有用。

如果你想[了解更多关于 Espruino](http://hackaday.com/2014/10/29/espruino-pico-javascript-on-a-usb-stick/) 的信息，你可能会喜欢更早的帖子(并查看下面 JavaScript/Espruino 驱动机器人的视频)。另一种流行的嵌入式[脚本语言是 Lua](http://hackaday.com/2013/06/28/bringing-elua-to-the-mbed/)——我们已经在运行它的 ESP8266】上做了[很多帖子。](http://hackaday.com/2015/01/01/a-dev-board-for-the-esp-lua-interpreter/)

 [https://www.youtube.com/embed/Yog0bIZPyJ0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Yog0bIZPyJ0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

