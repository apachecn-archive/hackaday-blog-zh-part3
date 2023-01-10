# 电路挑战:双晶体管 3.3V 稳压器

> 原文：<https://hackaday.com/2017/11/04/circuit-challenge-two-transistor-3-3v-regulator/>

[Kevin Darrah]想在不使用集成电路的情况下制作一个简单的 3.3V 稳压器。他最终使用了两个普通的 NPN 晶体管和 4 个 1K 电阻。该电路不会击败廉价的线性稳压器 IC，但对于低元件数，它实际上是相当不错的。

平心而论，虽然[Kevin]可能有两个晶体管，但他只是将其中一个用作合适的晶体管。这是一个传统的传递调节器，就像任何调节器电路一样。另一个晶体管只有两个连接点。该设计反向偏置基极-发射极结，产生大约 8V 的击穿电压。本质上，这个晶体管被用作低质量的齐纳二极管。

在正常温度下，传输晶体管将下降约 0.7V，因此将“齐纳晶体管”上的 8V 除以 2，得到另一个器件基极的 4V。降低 0.7V，最终得到 3.3v。[Kevin]做了一些快速测试，性能真的没有你想象的那么差。

如果你想了解 Zeners 的[问题，我们发布了相关内容。不过，请注意，根据帖子的定义，这里的齐纳二极管是用作参考，而不是调节器。我们还报道了](https://hackaday.com/2017/10/11/a-lesson-on-zener-regulators/)[Zeners](https://hackaday.com/2015/06/17/an-introduction-to-zener-diodes/)的一段视频。

 [https://www.youtube.com/embed/gu3ueRT0hco?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/gu3ueRT0hco?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

