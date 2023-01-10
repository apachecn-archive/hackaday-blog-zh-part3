# 真实世界 RF 滤波器设计和构造

> 原文：<https://hackaday.com/2017/03/30/real-world-rf-filter-design-and-construction/>

我们打赌，当[devttyS0]制作他关于 [RF 滤波器设计](https://www.youtube.com/watch?v=1sq8Cvju2Oo)的最新视频(YouTube，下面嵌入)时，他脑海中有一句老话:理论上，理论和实践之间没有区别，但在实践中，有区别。他首先指出，现在的现代工具将如何使设计和模拟任何类型的滤波器变得容易，但诀窍是在现实生活中实际构建它，并获得相同的性能。你可以看下面的视频。

当然，罪魁祸首之一是我们倾向于用完美的组件来设计和模拟。导线的电阻、电容和电感为零。在我们美好的设计世界里，电感和电容没有寄生元素。甚至元件的值也会偏离它们的理想值，并可能随时间而改变。

因此，[devttyS0]在电路的谐振部分使用微调电容。这样，您就可以根据电路变化进行调整。这不是唯一的实用建议。需要一个小电容？将一些电线缠绕在一起(我们听说过一种叫做“噱头电容器”的技巧)。

如果你一直喜欢[埃利奥特·威廉姆斯] [关于滤波器](https://hackaday.com/2017/03/29/dont-fear-the-filter-cascading-sallen-keys/)的帖子，你会发现有源音频滤波器和无源 RF 滤波器之间有很多不同，尽管有些想法是相同的。在频谱分析仪上实时观察不同电路调整的效果是非常有启发性的。您甚至可以看到使用屏蔽来分隔滤波器部分的效果。如果你真的想深入研究射频设计，你也可以看看来自迈克尔·奥斯曼的视频[。](https://hackaday.com/2016/03/23/michael-ossmann-makes-you-an-rf-design-hero/)

 [https://www.youtube.com/embed/1sq8Cvju2Oo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/1sq8Cvju2Oo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

