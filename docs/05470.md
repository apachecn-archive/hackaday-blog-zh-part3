# 右侧电路将多普勒模块转换为传感器

> 原文：<https://hackaday.com/2017/03/31/the-right-circuit-turns-doppler-module-into-a-sensor/>

12 美元能买到工作雷达模块吗？事实证明，你可以。但是你能让它输出有用的信息吗？根据[Mathieu]的说法，答案也是肯定的，但前提是你忽略数据手册中的电路，为你极其廉价的多普勒模块构建[这个放大电路。](http://www.limpkin.fr/index.php?post/2017/02/22/Making-the-Electronics-for-a-24GHz-Doppler-Motion-Sensor)

问题中的模块是一个 24 GHz 的 CDM324 板，目前在亚马逊上的价格是 12 美元。这是几年前我们报道过的项目中[的【马修】使用的 X 波段 HB100 的 K 波段表亲，但由于波长更短，模块要小得多——只有一英寸见方。[Mathieu]发现新模块存在数据手册中相同的误导性放大器电路。在进行一些调整后，设计了一个两级放大器，并在一个电路板上执行，该电路板通过 3D 打印的支架搭载在模块上。](https://hackaday.com/2013/08/14/making-the-electronics-for-a-doppler-motion-sensor/)

频率输出与被检测物体的速度成正比；传感器的最大速度只有 14.5 英里/小时(22.7 公里/小时)，所以不要指望跟踪任何东西太快。然而，这可能是一个方便的传感器，这绝对是一个坚实的设计教训。尽管如此，如果你的口味更倾向于在 1.25 厘米的火腿波段上使用这个模块，那么看看这个基于 HB100 的 3 厘米波段收音机。

 [https://www.youtube.com/embed/PCI9bbN7HsE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/PCI9bbN7HsE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

