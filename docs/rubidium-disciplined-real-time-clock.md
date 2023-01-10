# 铷训练实时时钟

> 原文：<https://hackaday.com/2016/09/25/rubidium-disciplined-real-time-clock/>

[卡梅伦·梅雷迪思]在他的一个项目的 Hackaday.io 页面上，引用了 Hackaday 的一篇文章:“*在硬件黑客的世界里，时计更像是一种仪式*”。我们袖手旁观的断言，但我们会说，我们的大多数时钟功能没有他的项目。他制作了由铷频标控制的实时时钟模块[，由于它还包括一个 GPS 时钟，他可以通过比较两者来跟踪当地的](https://hackaday.io/project/15070-rubidium-disciplined-real-time-clock)[时间膨胀](https://en.wikipedia.org/wiki/Time_dilation)效应。

过剩的铷标准很容易获得，但每一个描述似乎都有许多老式的硬件黑客只是为了让它工作。这一次也不例外，一个不寻常的连接器必须更换，并附加一个额外的电源模块。一旦进行了这些修改并安装了合适的散热器，他就能够将铷标准、RTC 模块和 GPS 模块与 ATMega32U4 微型 Arduino 兼容板和 LCD 显示器放在一起。固件功能正常，但他承认还没有完成。

所有项目的文件都可以在上面链接的 Hackaday.io 页面上找到。未来的计划还包括监测来自科罗拉多州科林斯堡的 NIST WWVB T1 无线电时间信号，以进行额外的时间膨胀比较。

这些年来，我们在 Hackaday 展示了无数的时钟，但其中有一些是基于原子标准的。不止一个[被用作实验室参考标准](http://hackaday.com/2015/07/23/hacking-a-telecoms-frequency-standard-for-your-lab/)，但与这个版本最相似的是【Max Carters】实验来检查原子标准的准确性，[也使用 WWVB 传输](http://hackaday.com/2015/05/27/measuring-accuracy-of-rubidium-standard/)。