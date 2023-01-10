# 独特的麦克风前置放大器

> 原文：<https://hackaday.com/2018/07/07/a-unique-microphone-preamp/>

我们生活在一个几乎任何你能想象到的小工具或工具都只需点击几下鼠标的世界里。在许多方面，这在过去十年左右的时间里帮助推动了创客文化；现在人们不再局限于当地可用的硬件，他们能够创造比以前更大更好的东西。但是它也有不利的影响。例如，人们不禁要问，当他们可以买到通常低于单个部件成本的东西时，为什么还要自己费心去制造呢？

批评家可能会争辩说，许多美化了 Hackaday 页面的项目可能会被商业上可用的同类项目所取代。我们不否认。但是购买交钥匙产品和自己打造替代产品的区别在于，你可以完全按照你想要的方式*制作*。这正是[[Sam Izdat]创造这款真正独一无二的麦克风前置放大器的原因。他会不会在网上买了一个更便宜的？大概吧。他能为自己节省大量的时间和精力吗？毫无疑问。我们在乎吗？一点也不。](https://imgur.com/a/HOEjseO)

该放大器基于德州仪器 INA217 芯片，采用 Arduino Nano 和 128×64 有机发光二极管显示器提供可视化效果。[Sam]花几块钱就能在易贝找到一个典型的 INA217 实现的裸 PCB(明白我们的意思吗？)，这帮助他起步，并允许他在软件方面花更多的时间。他的可视化代码提供了许多有趣的显示模式，使用了快速的 Hartley 变换，并且非常接近最大化 Arduino。

但也许这一建筑的任何元素都不如本案独特。设计背后的基本原理是[Sam]希望将设备的每个部分(电源、放大器、可视化)分隔开来，以避免任何干扰。圆柱形状是一个实用性的问题:隔间是通过使用孔锯制作木制圆盘，然后粘合在一起并挖空来建造的。该案件是染色和聚氨酯涂层，但由于一些稍微过度使用胶水和填料，颜色不均匀。这使得最终的作品看起来有些风化，与明显的高科技外观形成鲜明对比。

总的来说，这种构建让我们想起了今年早些时候看到的[模块化 3D 打印放大器](https://hackaday.com/2018/01/12/printed-pc-speakers-are-way-cooler-than-yours/)与这些[扬声器集成的 Arduino VU 仪表](https://hackaday.com/2015/11/29/this-vu-meter-is-built-into-the-speaker/)。

 [https://www.youtube.com/embed/hFIVMW1R0K4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/hFIVMW1R0K4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

