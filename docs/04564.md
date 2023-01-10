# 用 Z80 逆向计算 4 美元

> 原文：<https://hackaday.com/2017/01/02/retrocomputing-for-4-with-a-z80/>

当然，你想参与你在 Hackaday 上读到的所有逆向计算活动。但是买老式的硬件要花很多钱，对吧？当然，你可以自己建造，但是谁有时间去做一个大项目呢？[Just4Fun]有一个 Hackaday.io 项目，驳斥了这两个神话，不再给你任何借口。他的逆向计算机？一个 4MHz Z80，可以运行 64K RAM 的 BASIC 程序，所有这些都建立在一个带有 4 个 IC 的试验板上。成本？大约 4 美元。

当然，这是在易贝进行的一些电力采购，并假设你有一些常见的东西，如试验板，电线，小部件和电源。虽然它会激怒反对 Arduino 的人群，但[Just4Fun]使用 Arduino(嗯，一个带有 Arduino 引导加载程序的 ATmega32A)来代替 Z80 外围设备的主机。你可以在下面看到该设备的视频，在 Hackaday.io 项目页面上还有更多。

ATMega 用作时钟和复位发生器。它也是计算机的 EPROM。有一个独立的 RAM 芯片，但有一半没有使用(我们在这里闻到了银行切换模式)。你确实需要 CMOS Z80 芯片来与其他现代芯片如 ATMega 配合使用。

这是一个伟大的复古项目。我们不禁注意到芯片上的 IC 引脚标签，这是一个很好的触摸，以及开关和 led 上的标签。

【Just4Fun】不止一次做过[这种事情](http://hackaday.com/2016/10/01/hack-an-8085-like-its-1985/)。如果你想知道 ATmega 节省了多少芯片，你可以看看[这个版本](http://hackaday.com/2015/04/15/the-rum-80-a-home-brew-z80-computer-built-from-scratch/)。

 [https://www.youtube.com/embed/7eSbZ2Hu_6s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/7eSbZ2Hu_6s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

