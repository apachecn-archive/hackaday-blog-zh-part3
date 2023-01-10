# 一个女人用土豆制作了一个超高频振荡器

> 原文：<https://hackaday.com/2017/04/30/afroman-makes-a-uhf-oscillator-from-a-potato/>

如果你曾经使用过简单的逻辑门，很有可能在某个时候你已经用一串反相器构建了一个环形振荡器。通过增加一个电阻和一个电容，您可以用标准逻辑芯片轻松制作高达兆赫范围的方波振荡器。

[Afroman]收到了一些非常特殊的逻辑芯片，来自一家名字出乎意料的公司，土豆半导体。他们专门制造普通 74 系列逻辑的版本，打破了更快的传统 74 系列芯片通常 100+ MHz 的障碍，并将带宽扩展到 1 GHz 以上。使用他们的 74GU04 器件之一，[他制作了一个环形振荡器，仅依靠其栅极输入的杂散电容来定时](https://www.youtube.com/watch?v=8rRRvgjLjZU)，虽然他没有成功实现 GHz，但他确实在大约 373 MHz 处测量到了它。他用频谱分析仪看了一下，正如你可能从逻辑电路中看到的那样，发现了 GHz 范围内的强谐波。

通常情况下，用 7404 制作环形振荡器不会有什么新闻。它真的不会是一个普通的 74LS 或 74HC 部件的黑客。但是土豆的这一部分非常不寻常，它本身就值得引起一点注意。毕竟，我们不习惯能在这种频率下工作的逻辑芯片。

我们已经把他的视频放在休息时间下面了。与此同时，[土豆半导体网站](http://www.potatosemi.com/)提供了一个有趣的浏览，并证明了古老的 74 系列还有很多生命。

 [https://www.youtube.com/embed/8rRRvgjLjZU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/8rRRvgjLjZU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



我们之前已经展示过很多次 Afroman，最近一次是用简单的功率逆变电路和小型调频发射机展示[。我们期待着从这个多产的来源得到更多。](http://hackaday.com/2016/03/09/afroman-and-the-case-of-the-suspect-inverter/)