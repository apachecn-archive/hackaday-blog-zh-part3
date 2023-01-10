# SDR Pan 适配器

> 原文：<https://hackaday.com/2015/12/19/sdr-pan-adapter/>

业余无线电爱好者长期以来一直使用 pan 适配器来可视化整个无线电频谱范围。传统上，适配器本质上是一个频谱分析仪，它显示一条轨迹，其中 X 轴是频率，Y 轴显示任何特定频率下的信号强度。你一眼就能快速找到忙频或空频。

尽管 pan 适配器自 20 世纪 30 年代就已出现，但它们并不像你想象的普通模拟收音机那样普遍。但是，如果您使用了 SDR(软件无线电)，频谱显示是理所当然的。[Mehdi Asgari]做了很多火腿最近一直在做的事情:他将 SDR 和他的传统接收器结合起来，不费吹灰之力就提供了一个很棒的 pan 适配器。

要理解这种方法，你必须记住超外差接收机是如何工作的。混频器将可变频率与目标频率相加(或相减)。这将接收的频率转换到一个固定的频率，这样收音机就可以很容易地放大和过滤信号。[迈赫迪的]无线电，Icom R72，使用 70.45 MHz 的固定频率。这被称为中频或 IF。

[Mehdi]使用 PlaySDR，尽管即使是便宜的 RTL-SDR 加密狗也能在那个频率下工作。诀窍是找到一个地方，在不妨碍无线电工作的情况下，从接收器中获取中频信号。他找到了一个可能接入中频的地方，并使用一个小电阻来确保 SDR 输入不会加载无线电的中频级。然后，只需将一些 SDR 软件设置到 IF 频率，就有了一个 pan 适配器。如果你愿意，你甚至可以[使用 GNU Radio](http://hackaday.com/2015/11/12/your-first-gnu-radio-receiver-with-sdrplay/) 做一些定制的事情。

这不是原创黑客。然而，每个无线电需要一点不同的方法来获取 IF。例如，下面的视频显示了使用 RTL-SDR 加密狗和建伍 TS-570 进行的类似黑客攻击。

 [https://www.youtube.com/embed/Rn6pfI_2Mjc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Rn6pfI_2Mjc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

