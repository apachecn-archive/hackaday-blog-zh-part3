# 了解一下锁相环

> 原文：<https://hackaday.com/2018/06/20/learn-something-about-phase-locked-loops/>

锁相环(PLL)是电路设计中真正的主力。这是一个经典的反馈环路，利用误差信号将振荡器的相位锁定到参考信号的相位，其基本方式与物理系统中控制器保持温度或流量的方式相同。也就是说，大错误会导致大变化，小错误会导致小变化，直到输出恰到好处。[The Offset Volt]有几个关于 PLL 的视频，可以帮助你理解[它们的基本操作](https://www.youtube.com/watch?v=lT4SVnrdPkE)，它们如何倍频(矛盾的是，通过分频)，甚至解调 FM 无线电信号。你可以看下面的视频。

PLL 的巧妙之处在于它如何看待两个信号的相位。为了使信号完全同相，它们必须具有相同的频率，并且必须在同一点出现衰减和峰值。应该清楚的是，如果频率不一样的话，波峰和波谷不可能在任何时间长度内都保持一致。通过检测信号不对齐的程度，可以产生一个误差电压。该误差电压用于调整输出振荡器，使其与参考振荡器相匹配。

当然，如果输出频率必须与参考频率相同，那就没什么意思了。巧妙之处在于对输出频率进行分频。例如，100 MHz 晶体振荡器很难设计。但是，采用 100 MHz(标称值)的压控振荡器，将其输出除以 100，将得到一个可以锁定到 1 MHz 晶体振荡器的信号，当然，构建这种振荡器并不重要。

真正的细节在于相位比较和环路滤波，一旦你看了视频，这将更有意义。

根据视频浏览量来看，[偏移电压]可能是最好的 YouTube 频道，人们不怎么看。视频清晰易懂！他甚至提到了一种自密封阀杆螺栓，因此我们不禁对此印象深刻。

我们的常驻视频明星[Bil Herd]不久前在 PLL 上做了一次[演讲。如果你更想阅读并想了解软件](https://hackaday.com/2011/06/21/pll-101/)中的[PLL 是如何工作的，我们也已经讨论过了。](https://hackaday.com/2017/09/10/a-great-guide-to-software-plls/)

 [https://www.youtube.com/embed/lT4SVnrdPkE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/lT4SVnrdPkE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/5by0os8RrFY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/5by0os8RrFY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/j1_D704Mh3s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=10&wmode=transparent](https://www.youtube.com/embed/j1_D704Mh3s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=10&wmode=transparent)

