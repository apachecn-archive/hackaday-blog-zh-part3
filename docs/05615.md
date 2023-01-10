# Z80 Fuzix 就像老式的 Unix

> 原文：<https://hackaday.com/2017/04/16/z80-fuzix-is-like-old-fashioned-unix/>

经典的 Z80 电脑倾向于运行 CP/M。如果你是一个纯粹主义者，你会很高兴，因为这肯定是最严重的 Z80 电脑在一天跑回来。不过实际使用起来，这年头 CP/M 确实感觉过时了。Linux 更舒适，但不太可能在 Z80 上运行。或者是？Linux 借鉴了 Unix，早在 20 世纪 80 年代，Doug Braun 就为 Z80 编写了一个类似 Unix 的操作系统 UZI。这些年来已经有了很多分支，一个名为 [FuzixOS](https://github.com/EtchedPixels/FUZIX) 的项目旨在开发一个有用的 Z80 Unix 类操作系统。

当然，1980 年的 Unix 与现代的 Linux 有很大不同，但它仍然比 CP/M 更接近现代系统。Fuzix 还添加了几个现代功能，如 30 个字符的文件名和最新的 API。顺便说一下，内核不仅仅是 Z80 的。它可以针对各种旧处理器，包括 6502、6809、8086 等。如您所料，该系统可以放入一个非常小的系统中。

下面的视频显示了运行 Fuzix 的[Scott Baker]RC 2014 计算机。您会看到它看起来很像 Linux 系统，尽管这种类比仅限于此。

尽管内核非常易于移植，但是存在一些工具问题。根据 Fuzix 页面，它没有 8086 编译器，并且对其他一些 C 编译器有限制。然而，有大量的平台在工作，包括 Amstrad、Atari、Radio Shack 计算机、N8VEM 板等等。

我们总是很惊讶我们没有看到更多运行 MINIX 的复古计算机，MINIX 是过去常见的 Unix 替代品。如果你有兴趣了解更多关于 RC2014 的信息，我们[为你回顾了](https://hackaday.com/2016/09/08/review-the-rc2014-z80-computer/)。

 [https://www.youtube.com/embed/1WG8zopGzaA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/1WG8zopGzaA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

