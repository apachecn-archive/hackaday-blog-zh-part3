# 世界上有 10 种电脑

> 原文：<https://hackaday.com/2017/12/18/there-are-10-kinds-of-computers-in-the-world/>

有个老笑话说世界上有 10 种人。懂二进制的，不懂的，没看到一个基三笑话来的。也许[德米特里·索科洛夫]听过这个笑话，因为他已经建造了一台三进制计算机。他声称这是过去 50 年来建造的第一座。你可以在下面看到一个关于这个设备的视频。还有一个带有数码管输出的设备视频。

你可能不会经常想到，但是 *bit* 是二进制数字的缩写，所以三进制计算机没有那些。它有 trits。CPU 对 3 个 trit 字进行操作，只使用多路复用器作为构建模块。指令使用 5 个 trit，其中一些是 13 个寄存器之一的 2-trit 操作码和 3-trit 地址。顺便说一句，使用三进制的魅力在于，你可以用更少的位数表示更多的数字——嗯，更确切地说是 trits。

这可能看起来是奇数个寄存器，但使用平衡三进制，一个 3 trit 字可以表示从-13 到 13 的数字，所以它是有意义的。平衡 trit 有-1、0 和 1 状态，而不是位的 1 和 0 状态。为了防止混淆，[Dmitry]在谈论三进制单词时使用 N、0 和 P 这三个符号。比如 101 在他的记数法里就是十进制 10 或者 P0P。要表示-10，只需使用 NoN。

多路复用器使用模拟开关 DG403。我们之前讨论过用多路复用器制作逻辑门，但是——当然——那是二进制的。然而，我们不太确定这真的是 50 年来的第一次，因为我们记得有一次 Hackaday 奖的参赛作品与[相似](https://hackaday.com/2014/06/02/the-hackaday-prize-a-ternary-computer/)。事实上，这位设计师在去年的[黑客日超级大会](https://hackaday.com/2016/12/16/building-the-first-ternary-microprocessor/)上发表了一篇关于她的 CPU 的演讲。尽管如此，这仍然是一件令人印象深刻的作品。

早在 20 世纪 50 年代，俄罗斯人就在这一领域做了大量工作。如果你能看懂一点俄语，你可以随时去网上试试他们的模拟器。

 [https://www.youtube.com/embed/VCJHS836rlI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/VCJHS836rlI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/3ijeF--3y5Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/3ijeF--3y5Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

