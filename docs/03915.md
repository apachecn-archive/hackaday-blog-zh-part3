# 仿人工智能克拉珀几乎似乎在听

> 原文：<https://hackaday.com/2016/10/24/faux-ai-clapper-almost-seems-to-be-listening/>

当一项工作可以用微控制器来处理时，[devttys0]喜欢逆潮流而动，建立一个不需要编码的电路。这个受“拍板”启发的人工智能灯光控制器就是如此，它最终成为模拟设计中的一个伟大教训。

我们的目标是创造一个穷人的 JARVIS——用自由形式的声音命令打开工作室的灯。或者，至少让它看起来是这样。这是一个全模拟电路，带有一对运算放大器和一对比较器，因此它实际上无法处理所说的内容。“阿齐兹！轻！”因为电路根据口头命令的幅度和持续时间触发。AI-lite 效果来自对比较器、控制延迟的 RC 网络以及由分立 MOSFETs 构成的与门的巧妙使用。最终的结果是一个电路，它会等到你说完话才触发灯，让它看起来好像真的在分析你说的话。

我们一直很喜欢[devttys0]的视频，因为它们是电路设计的绝佳课程。从框图到完成的原型，一切都以逻辑步骤呈现，总有东西要学。他展示数学概念的模拟电路让我们大开眼界。如果你想了解激发这一建筑灵感的 20 世纪 80 年代人工智能技术的一些背景知识，可以看看[最初的“拍板者”](http://hackaday.com/2013/09/29/inside-the-clapper/)。

 [https://www.youtube.com/embed/tRDRDCbZyqw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/tRDRDCbZyqw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

