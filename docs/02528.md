# 设计单指令计算机

> 原文：<https://hackaday.com/2016/06/11/designing-a-single-instruction-computer/>

今天的计算机复杂得难以想象，而且如此复杂以至于任何人都几乎不可能以令人痛苦的细节理解 CPU 所能做的一切。它并不总是这样——70 年代和 80 年代的早期 CPU 相对简单，可以很容易地在单个门级别上重新创建。CPU 甚至可以更简单，正如[Jack Eisenmann]用一台单指令计算机展示的[，DUO Compact 2，完全由 74 系列逻辑芯片和一堆内存组成。](https://www.youtube.com/watch?v=dgYmDwcRrAQ)

[杰克]拥有用单个芯片建造奇怪计算机的悠久历史，包括[一个 TTL 逻辑 CPU](http://hackaday.com/2011/06/17/homebrew-ttl-logic-computer/)和[一个明显更复杂的单指令计算机](http://hackaday.com/2012/09/05/mess-of-wires-is-actually-a-one-instruction-computer)。然而，最新的一个非常简单。它只有 20 个芯片，能够计算素数，排序字符串，以及计算机能够做的一切事情。

每一台单指令计算机都有一个明显的问题，就是这台计算机使用什么指令。对于 DUO Compact 2，它是一条接受三个参数 A、B 和 c 的指令。该指令将一个字节从 A 复制到 B，然后跳转到 c 处的指令。计算机有可能用这条指令将两个数字相加吗？是的，如果你有大量的查找表存储在 2 兆的闪存和 512 kB 的内存中。

在下面的视频中，[Jack]讲述了他的微型计算机是如何工作的，并演示了质数生成(它很慢)、字符串排序(也很慢)，以及在计算机的 LCD 上显示“墙上有 99 瓶啤酒”。复制这台电脑[的所有文件都可以在【Jack】的网页](http://ostracodfiles.com/compact2/main.html)上找到，同时还有一个模拟器，以防你不想为这台电脑准备一个试验板。

 [https://www.youtube.com/embed/dgYmDwcRrAQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/dgYmDwcRrAQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

