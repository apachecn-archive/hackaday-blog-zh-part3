# 振荡器的模拟设计

> 原文：<https://hackaday.com/2016/03/22/oscillator-design-by-simulation/>

[克雷格]想要制造一个 19.2 兆赫的晶体振荡器。他知道自己想要一个皮尔斯振荡器，但他也知道获得一个好的设计往往需要反复试验。他使用了一个专业模拟包(是德科技的 Genesys)的 30 天试用版，来观察振荡器的性能，而无需构建任何东西。他不仅写了一篇关于他经历的精彩文章，还做了一个很棒的视频演示(见下文)。

该工具生成了一个示例原理图，尽管[Craig]删除了它，并将他自己的设计放入了模拟器中。通过运行模拟，他能够观察振荡器的性能。他的第一次切割表明，电路不符合巴克豪森标准，不应该振荡。不幸的是，他的原型，事实上，振荡。

[Craig]解释了为什么初始仿真(开环)与真实电路不匹配，这很有启发性。通过使用兰德尔和霍克论文中的一个等式，他能够得到一个更真实的模拟。

我们之前已经讨论过[振荡器基础](http://hackaday.com/2015/08/01/everything-you-wanted-to-know-about-oscillators/)，但是【Craig 的】专业工具的视频演示太棒了，不容错过。如果你负担不起 Genesys 4700 美元的基础价格(选项是额外的)，你可以试试 [Spice](http://hackaday.com/2016/02/26/adding-spice-to-your-workbench/) 。

 [https://www.youtube.com/embed/RfZZGsR_KlQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/RfZZGsR_KlQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

