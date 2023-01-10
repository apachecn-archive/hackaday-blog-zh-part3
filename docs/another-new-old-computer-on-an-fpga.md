# FPGA 上的另一台新的旧计算机

> 原文：<https://hackaday.com/2017/12/01/another-new-old-computer-on-an-fpga/>

你会如何向潜在买家销售电脑？快速？靠谱吗？出色的图形和声音？1956 年，你可能会指出它比一张桌子还小。毕竟，在那个时代，人们认为计算机是庞然大物。多亏了现代 FPGAs，你现在可以拥有一台 1956 年的电脑-LGP-30 的复制品，它比一张桌子小得多。LittleGP-30 是[于尔根·米勒]的创意。

最初的重量也约为 740 磅，不到 336 公斤，所以 FPGA 版本在质量上也占优势。LGP-30 相对苗条的足迹归功于它仅使用了 113 根管子，其中只有 24 根管子在 CPU 中。这是可能的，因为像许多早期的计算机一样，CPU 一次处理一位。虽然现代计算机会一次添加一个单词，但这台计算机——甚至是 FPGA 版本——会一次一位地添加每个操作数。

LGP-30 有一个 Friden Flexowriter(一种类似电传打字机的机器，由一家最终被缝纫机公司 Singer 收购的公司制造)和一个带有 4096 个 32 位字的磁鼓。为了减少组件数量，鼓存储了程序、CPU 寄存器，甚至 120 kHz 系统时钟。还有 1450 个固态二极管，这也有所帮助。为了避免制造大量闪烁的灯，前面板有一个显示三个寄存器的示波器。大约有 500 个单元以大约 47，000 美元售出。

幸运的是，FPGA 版本更便宜。它使用 Xilinx Spartan 6 开发板和定制 PCB，甚至可以在 LCD 上复制示波器。您可能会注意到示波器上有一些奇怪的字符。即使计算机使用十六进制(这在当时是不常见的)，它也没有使用 A-F 作为额外的数字。相反，它使用了有限的硬件更容易解码的字符:f，g，j，k，q 和 w。所以 LGP-30-speak 中的 255 是 ww 而不是 FF。

尽管 FPGA 版本可靠、廉价、小巧，但它并不是该架构的第一个固态版本。librascope——LGP-30 背后的公司在 1963 年推出了 LGP-21，它只有不到 500 个晶体管和 300 个二极管。不过，它没有 LGP-30 快，而且价格只有区区 16200 美元。再说一次，FPGA 板的成本不到 40 美元，尽管前面板和外壳会提高价格，但它仍然会低于这个价格。如果你想一窥真机内部，看看下面的视频。

任何时候我们看到位串行 CPU，都会让我们想起 [EDSAC](https://hackaday.com/2017/10/05/learn-fpga-programming-from-the-1940s/) 。我们感兴趣的一件事是，如果当时的黑客有计划的话，113 管机器应该在他们的能力范围之内。例如，1967 年，人们确实用大约 400 个晶体管建造了[无线世界计算机](https://hackaday.com/2015/10/29/400-transistors-and-1800-resistors-form-this-1967-personal-computer/)。

 [https://www.youtube.com/embed/FGDGpCWWoMs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/FGDGpCWWoMs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

