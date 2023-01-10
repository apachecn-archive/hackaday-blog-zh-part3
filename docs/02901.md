# 五十欧姆有什么特别的？

> 原文：<https://hackaday.com/2016/07/11/whats-special-about-fifty-ohms/>

如果你使用过无线电或其他高频电路，你可能已经注意到 50 欧姆同轴电缆的流行。当然，你有时会看到 75 欧姆同轴电缆，但绝大多数情况下，射频电路工作在 50 欧姆。

《微波 101》有一篇有趣的文章，讲述了这是如何成为无处不在的比赛。显然，在 20 世纪 30 年代，无线电发射机正朝着更高的功率水平发展。你一般认为电线越粗损耗越小。不过，对于承载 RF 的同轴电缆，情况就有点复杂了。

首先，RF 信号表现出趋肤效应，它们不会在导体中心传播。第二，电介质材料(即内外导体之间的绝缘体)起作用。阻抗也是电介质材料和中心导体直径的函数。

当你把所有这些放在一起时，你会发现对于空气绝缘的电缆，77 欧姆的电缆损耗最小。当然，那不是 50 欧姆，对吧？它接近于电视系统中用于传输微弱天线信号的 75 欧姆。根据[微波 101]，这不是原因——这与使用廉价的钢代替铜作为中心导体有关。

传输是不同的。你想掌握你所能掌握的最高权力。同一根电缆的峰值功率处理因阻抗而异。因此，77 欧姆时损耗最小的电缆在 30 欧姆时也具有最大的功率处理能力。30 和 77 欧姆之间的平均值为 53.5 欧姆。

如果你想了解更多关于 RF 设计的知识，你可以去看看[【迈克尔·奥斯曼的】研讨会](https://hackaday.com/2016/03/23/michael-ossmann-makes-you-an-rf-design-hero/)(见下文)。如果你对同轴电缆终端更感兴趣，我们[也为你提供](https://hackaday.com/2016/03/31/co-exist-with-your-coax-choose-the-right-connector-for-the-job/)服务。

 [https://www.youtube.com/embed/TnRn3Kn_aXg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/TnRn3Kn_aXg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

