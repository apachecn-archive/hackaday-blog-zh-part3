# 新的一天:坡道冰沙

> 原文：<https://hackaday.com/2016/11/14/new-part-day-smoothie-for-ramps/>

当谈到 3D 打印机控制器时，有两个主要的思想流派。第一组是 RAMPS 或 RAMBo，它们分别是 Arduino Mega 的 3D 打印机控制器“盾牌”和独立的控制器板。很长一段时间以来，这些主板一直是 DIY 3D 打印机的标准，也是许多大型制造商的打印机的大脑。另一个学派沿着 ARM 的道路前进，最流行的主板运行 Smoothie 固件。使用 ARM 微控制器运行打印机有很多优势，SmoothieBoard 非常棒。

本周上线的 Kickstarter 是这两种观点的中间立场。这是一个用于斜坡的主板，但它带来了 32 位 LPC1768 ARM 处理器的能力，实现了 SmoothieBoard 带来的所有平滑加速、精细控制和扩展能力。

用更小的董事会来经营思慕雪并不是什么新鲜事。在纽约 Maker Faire 的几个月里，[我们参观了 Cohesion3D](http://hackaday.com/2016/10/05/tiny-smoothies-at-maker-faire/) 的产品，这是一家致力于制造微型 32 位打印机控制器的公司。 [Smoothie 甚至已经移植到其他微控制器](http://smoothieware.org/third-party-branches)，ST 也正在用他们自己的开发套件进入 ARM 游戏[。](http://hackaday.com/2016/07/19/new-part-day-sts-32-bit-3d-printer-controller/)

尽管基于 ARM 的 3D 打印机控制器板的生态系统不断增长，但有一个缺点:RAMPS 几乎是一个标准。不过，对于 Arduino Mega 来说，这实际上是一个突破性的主板，这使得用手臂取代主板的“大脑”变得很容易。为什么没有人想到把一个兼容思慕雪的微控制器放在一个专为斜坡设计的电路板上，这让我无法理解；这是一个显而易见的创新。

重新武装将配备所有功能，你期望从一个板设计来控制坡道板。USB 插头是一个迷你 B，而不是 1998 年的大 B 插头(一个改进，但 *bruh，微型 USB* )。支持一个加热床和两个用于 hotends 的 MOSFETS，电源输入可以处理高达 30V 的电压。因为 Smoothie 固件和 SmoothieBoard 比您的标准 RAMPS 设置多了一些功能，以太网可与分线板一起使用，令人印象深刻的图形液晶显示器是一个附加组件。当然，像所有的奶昔板一样，配置就像在 SD 卡上添加一个文本文件一样简单。

基于 Arduino 的 3D 打印机控制器和 Makerbot 一样早就出现了，今天 RAMPS 已经非常接近标准了。有成千上万的打印机在 RAMPS 板上运行，但是 32 位 ARM 板才是未来。Re-ARM 为这些打印机提供了一个相当简单的升级途径，不需要购买新的步进电机，也不需要花费时间为打印机完全重新布线。这是对当前 3D 打印机控制器板的一个很好的补充，我们希望这个项目取得应有的成功。