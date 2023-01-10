# 用于表面安装部件的改进的穿孔板

> 原文：<https://hackaday.com/2018/01/09/improved-perfboard-for-surface-mount-parts/>

回顾过去二十年基于 perfboard 的电子项目，您会注意到一个趋势。Perfboard 设计用于通孔器件，但更常见的是，我们需要的器件只能作为表面贴装器件使用。这对所有这些原型板、veroboard 和 tagboard 设计的未来意味着什么？不好，不过还好，可能有答案。[它是为安装 SOICs、sot 和其他表面贴装器件而设计的 perfboard】。](http://www.eevblog.com/forum/manufacture/improved-protoboardperfboard-for-direct-soic-mounting/)

Perfboard 是一个极其简单的概念。大多数通孔电子元件的引脚间距约为 0.1”或 2.54 毫米。是的，也有例外，但你总是可以弯曲晶体管的中间引脚，并将其放在一个孔中。SMT 器件则不同。你不能真正弯曲引脚，引脚间距对于传统性能板中的 0.1”孔来说太小。

[electronic_eel]正在用他自己的 perfboard 设计改变这个游戏。这种性能板具有传统的 0.1”孔，但在这些孔之间散布着 SMD 焊盘。结果是能够将 SOIC、SOT23-6、SOT23 和 SOT363 器件与 0603 和 0805 器件一起直接焊接到电路板上。用一些焊料珠连接所有的东西，你就有了一个由表面贴装器件制成的功能电路，它仍然与旧的原板设计兼容。

这不是我们第一次看到一种新型的原板投入生产。几年前， [Perf+，一种奇异的“基于总线”的原板解决方案](https://hackaday.com/2015/04/05/ask-hackaday-the-latest-advances-in-perfboard/)出现了，尽管它并不是真正为 SMD 器件设计的。虽然[electronic_eel]没有出售他的原型板的任何计划，但是[的文件是可用的](https://github.com/electroniceel/protoboard)，你可以很容易地设计出你自己的小块 perfboard。