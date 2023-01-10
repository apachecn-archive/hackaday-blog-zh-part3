# FPGA 从垃圾箱中拯救范围

> 原文：<https://hackaday.com/2017/06/01/fpga-rescues-scope-from-the-dumpster/>

我一直在寻找一个符合我严格预算的高质量实验室。最近，我发现自己在做的每一个其他项目中都突破了赫兹的障碍，因此迫切地想要一个高带宽的范围。不幸的是，直到最近，70 MHz 至 100 MHz 才变得真正负担得起，而 500 MHz 至 1 GHz 范围内的新型四通道示波器仍然需要花费大量资金才能获得。我唯一的选择是找到一个绝对的奇迹，一个老式的高带宽示波器。

当我找到这个指定为 HP 54542C 的垃圾箱时，似乎上帝在向我微笑。它看起来状态非常好，是当时的老大。但总要打破一些东西，对吧？果然，屏幕明显有问题，难以辨认。想知道我是怎么修好的吗？四个字母:FPGA。

![](img/bb8548f04b24529523c48aad50335881.png)

The Problem

对这个范围的一些肤浅的研究揭示了一些有趣的历史。这应该是惠普的第一个带 LCD 的高端示波器，也是后来统治市场的 Infiniium 系列示波器的前身。液晶显示器确实感觉像是后来才想到的。示波器有一个完全相同的版本，带有 CRT 显示器，我得到的版本只是去掉了 CRT 接口，安装了惠普的彩色 LCD。我希望是液晶显示器出了问题，而不是 ASIC 在驱动它，这似乎是一个很好的赌注，因为轻轻的点击有时会让屏幕恢复生机！

我开始调查根本原因，并从拆开液晶屏开始。我发现上面溅满了液体；没有任何东西被腐蚀，但是清洗和重新安装没有任何影响。把瞄准镜和垃圾箱合二为一不是一个选择，因为除了液晶显示器，瞄准镜感觉就像一个绝对的宝库。尽管 LCD 的驱动板现在已经完全没有用了，但它来自一个行业还没有发展到线对板连接器的亚原子引脚间距的时代。这意味着我可以方便地在标准 26 针带状电缆上焊接，以分接所有需要的信号，并开始对使用中的协议进行逆向工程。

## 对 LCD 协议进行逆向工程

![](img/664dff0a87febeae764115cf3d73feb5.png)

Ribbon cable soldered on top of the existing connector

该过程的第一步是确定连接器上的信号。我在寻找驱动任何 LCD 所需的最普通的信号。这必须包括几个严格的周期信号，几个有点随机的信号，当然还有通常的电源和地。周期性信号很可能是像素时钟和同步信号，其将标记新的行和帧的开始；另一方面，看起来随机的信号将是要显示的实际像素数据。从它的年代来看，应该有一个相当简单的协议。在这种直觉的指引下，我开始探测连接器，很快我就弄清楚了所有的 25 个信号。

我只发现了两个完美的周期信号:一个是相对较低的 31.25 kHz 信号，选通在可疑的 60 Hz，另一个是 25 MHz 方波。前者必须是组合的同步信号。60 赫兹是一个绝对的泄露，因为它符合标称帧速率。于是，31.25 kHz 的基础信号必须对应于一帧内的水平行频。最后，25 MHz 信号必须是整个系统的时钟，事实上它是像素时钟。

接下来，我必须理解那些看起来随机的信号，它们显然是像素数据。首先，对 25 针连接器的需求显然暗示了某种并行 RGB 配置。我总共找到了 9 个这样的信号，它们完美地将除以 3，并得出结论，LCD 每像素使用 9 位，每颜色通道 R、G 和 B 分别使用 3 位。

![](img/ae8d6c3e64567f9f9def6fe71eb1dc88.png)

Example: VGA porch scheme

找出计划和牵制是挑战的一部分。也许更重要的是确定使用信号的时间。几乎总是，原始显示信号有所谓的“门廊”。这些可以被认为是每个帧中不能写入数据的区域。这些起源于 CRT 时代，在 CRT 时代，物理电子束需要时间从一行的末端扫回到另一行的开始，甚至从屏幕的底部扫到顶部。虽然在现代电子屏幕上不太明显，但这些区域仍然存在，因为 LCD 控制器需要时间来处理和混洗输入的数据。

## 确定时间

为了提取时序，我尝试将像素数据与同步信号相关联。我在寻找那些像素始终未被断言的区域。

![](img/478f8777eec002a4d4c17f2a4a248fa9.png)

Horizontal Timings

盯着数据看了一会儿后，很明显，LCD 对组合同步信号的水平和垂直部分使用了简单的单边沿方案。这很容易确定，因为在此期间像素被设置为全高或全低。一旦我确定了这些区域，我就使用光标来测量它们的持续时间，并将该时间转换成相等的像素数。

这是一条重要信息，可确保 VGA 显示器上的稳定和正确再现。计划是将这些值作为常量输入 Verilog，并使用计数器“触发”相应的逻辑以获得所需的波形。

![](img/4453cd94530791a246808ba5188a1fba.png)

Vertical Timings

最后，必须确定液晶显示器的分辨率，因为我必须在相同的设置下运行替换显示器。这是通过简单地测量各种活动周期并将它们与其他信号(例如周期为 40 ns 的像素时钟)进行比较来实现的。测得水平有效时间约为 25.7 us，因此总共由 642.5 个像素组成，类似地，垂直有效周期为 15.42 ms，水平周期为 30 us，相当于 481 行。显然，这是一个标准的 640 x 480 显示器，刷新率为 60 赫兹。

## 找到一个能干的替代者

![](img/44d21bbd271f8e3aca146552c6081f93.png)

The 8 inch Saviour

因此，现有的显示器最终被证明是非常普通的，一个替代品似乎完全可行。不幸的是，大小有点奇怪；很容易找到七英寸的屏幕，但是八英寸呢？尽管我在网上找不到任何价格合理的替代品，但它的尺寸恰好与许多现代汽车售后市场上安装的 LCD 相同。这些是很好的便宜的“EYOYO”品牌显示器(50 英镑),可以接受从所有模拟到 VGA 甚至 HDMI 的几乎所有形式的视频输入。它们还支持 1024 * 768 的更高分辨率。我很惊讶这个屏幕在 Raspberry Pi 社区中并不流行。

最后，一切似乎都合二为一了。我不仅可以用这个 VGA 显示器取代 LCD，它还可以完美地适应，因为示波器甚至有足够的空间来放置 CRT！

确切地说，如何实现 LCD 到 VGA 的转换呢？当然是用 FPGA！

## 信号变换

在这一点上，唯一站在我和一个正常工作的 500 MHz 示波器之间的是成功地将上述 LCD 信号转换成 VGA。很明显，这种相对快速的处理只能在 FPGA 上完成，但是是哪一个呢？我的意图是，在某种程度上，将 FPGA 留在屏幕范围内，所以我需要一些小而便宜的东西。幸运的是，易贝似乎有一吨[这些旧的基于 Altera Cyclone II 的开发板](http://www.ebay.co.uk/itm/ALTERA-FPGA-Cyslonell-EP2C5T144-Minimum-System-Learning-Development-Board-AS-/292042601272?var=&hash=item43ff187338:m:m_0gvptzkBHvaVCdkQVTgxQ)用于令人难以置信的 10！这些都是相当有能力的 FPGA，托管约 4K 逻辑元件和像这样的小规模项目的理想选择。

执行这些显示转换的常见方式是使用帧缓冲器。想法是缓冲整个帧，执行转换，并在另一端将其吐出。不幸的是，这要求 FPGA 上有相当大的外部 RAM。这些 FPGA 板因没有任何外部 RAM 而臭名昭著，因此这种方案是不可能的。经过一番思考，我意识到 LCD 信号和 VGA 并没有什么不同。如果我可以一行一行地从一个转换到另一个，并且完全不需要帧缓冲，那会怎么样？

![](img/6cf482eccbdd02ed83c9f3086ddb3c9f.png)

Comparasion: VGA vs LCD. This diagram applies to both the Horizontal and Vertical segments

总而言之:

LCD 具有:

*   像素时钟
*   组合同步信号
*   仅前廊

而 VGA 具有:

*   无像素时钟
*   分离同步信号
*   具有同步周期的前后沿

![](img/830aea97d29d72dea47f882ed40573c6.png)

The combined synchronisation signal

深入研究 VGA 的工作原理超出了本文的范围，但是我将在以后解决这个问题。现在，如果我们简单地检查一下时序示意图，我们会发现两个信号之间的唯一区别是出现的次数、门廊的位置以及有效数据的位置。

草图使转换看起来很简单，但只有在两个帧完全同步的情况下才有效。要让 FPGA 开始通过 VGA 产生相应的 LCD 帧，我们必须首先确定来自 LCD 连接器的新帧的起始位置，以便与之同步。这可能是这个过程中最棘手的部分，因为仅仅检查来自 LCD 的组合同步信号的边沿是不够的。

相反，我们必须测量两个边缘之间的时间，并标记新帧的出现。剩下的是一组相对简单的逻辑门，产生上面的时序图。最后，由于 LCD 没有后沿或同步脉冲，输入的 RGB 数据必须使用一个微型 FIFO 及时偏移，以便在 VGA 监视器期望的位置完美对齐。一旦将上述内容翻译成 Verilog，我就着手处理硬件。

## 硬件设置

![](img/3ca9b82e95168daf0bc49e999c2a6b84.png)

The Hardware Setup

幸运的是，硬件设置非常简单。惠普没有充分利用液晶显示器的潜力。检查每个通道的单个位会发现很多冗余:各个位几乎总是相同的，这表明整个九位调色板的利用率非常低。这并不令人震惊，因为惠普主要是重用 CRT 版本的示波器的固件。所有这些意味着我只需连接每个颜色通道的 MSB，最终图像几乎没有任何损失。这为我节省了更多宝贵的 FPGA 内存。

最大的问题是 LCD 使用 5 V TTL 信号。FPGA 最多可以接受 3.3 V 信号，因此必须执行电平转换。我决定利用一些 74HC 系列逻辑缓冲器中的输入箝位二极管来执行这一转换。然而，这往往会严重破坏上升/下降时间。例如，74HC4050 甚至在芯片中有与二极管串联的多晶硅电阻，从而不再需要外部串联电阻。为了安全起见，我在这些缓冲器的输入端增加了 1kω串联电阻，的输出馈入 FPGA。FPGA 的 HSYNC 和 VSYNC 输出直接连接到监视器，而 RGB 线通过 330ω电阻连接。

## 成功

![](img/d5239408efa054dea563eab40e013a58.png)

Success!

在驯服 25 MHz 像素时钟以在试验板上运行并将 FPGA 连接到新的外部设备之后

显示器的 VGA 口，示波器恢复了它的正式荣耀！虽然一切都很完美，但这种设置很容易产生噪音。我现在需要做的就是制作一个 PCB，并授予 VGA 显示器在示波器内的永久驻留权。

你接下来会问什么？嗯，目前保存截图的唯一方法是通过一个过时的软盘驱动器。但是既然我们现在已经让 LCD 数据通过 FPGA，为什么不把它写到 SD 卡呢？