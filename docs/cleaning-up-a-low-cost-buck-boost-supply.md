# 净化低成本降压升压电源

> 原文：<https://hackaday.com/2017/10/10/cleaning-up-a-low-cost-buck-boost-supply/>

廉价的 DC-DC 转换器已经成为业余爱好者的福音有一段时间了，但如果不小心，它们可能会对敏感电路造成严重破坏。问题是:开关模式电源产生的噪声隐藏在其中。你能对噪音做些什么吗？

事实证明，答案是肯定的，信号路径的[Shahriar]带我们了解了降低 DC-DC 转换器噪声的基本电路。手术刀下的模块是一个流行的降压升压转换器，具有宽输入范围，0-32 VDC 输出，最高 5 安培，以及一个带 LCD 显示器的奇特控制器。但是，将 32 美元的库存电源放在示波器上，会发现 1 MHz 频带内有大量谐波，总纹波约为 66 mV。但由功率运算放大器和齐纳二极管构建的简单电压跟随器在减少尖峰和将纹波减半方面表现出色。该电路只是一个原型，更多的是作为原则的证明和进一步发展的起点，因此它远非完美。主要缺点是与输入电压有 4 伏的偏差；在频谱的高端还有一个广泛的噪声拖影，即使电路就位也仍然存在。~~因为它集中在 900 MHz 附近，我们怀疑某种手机信号正在进入。~~ 900 kHz。

如果你还没看过信号路径上的视频，你真的应该看看。[Shahriar]在解释 RF 工程中的高级主题方面很有一套，并且有一个非常值得拥有的工作台。我们之前报道过他的一些项目，从[抢救一台价值 2700 美元的频谱分析仪](https://hackaday.com/2017/01/29/2700-ebay-bet-pays-off-for-this-14-ghz-spectrum-analyzer-repair/)到[复用光纤传输](https://hackaday.com/2012/06/04/color-multiplexing-through-fiber-optics/)。

 [https://www.youtube.com/embed/DPN1BERe6cg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/DPN1BERe6cg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

