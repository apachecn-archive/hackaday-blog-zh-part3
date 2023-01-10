# Hackaday 奖参赛作品:宇宙粒子探测器是伪装成艺术的公民科学

> 原文：<https://hackaday.com/2017/06/09/hackaday-prize-entry-cosmic-particle-detector-is-citizen-science-disguised-as-art/>

多亏了欧洲粒子物理研究所和他们使用大型强子对撞机(LHC)探测希格斯玻色子的工作，许多人对了解更多关于宇宙基本组成部分的兴趣激增。欧洲粒子物理研究所能够做到这一点是因为 LHC 的巨大能量——能够达到近 14 兆电子伏的束能量。与此相比，一些宇宙射线的能量高达 3×10 ^ 20 T2 eV ^ T3。而这些宇宙射线不断向地球倾泻而下，当它们与大气分子相互作用时，会产生粒子的连锁反应。当许多这些粒子到达地球表面时，它们已经变异成“μ子”，可以使用盖革-米勒管(GMT)检测到。

[罗伯特·赫德]正在建造一个由单个宇宙射线探测器组成的阵列,这些探测器可以分布在整个景观中，以显示这些宇宙射线(严格来说是粒子)是如何以μ子簇射的形式到达的。这是一个伪装成艺术装置的公民科学项目。

每个单独设备的核心将是一组三个俄罗斯盖革-米勒管，用于检测粒子，以及一个 RGB LED，根据检测到的粒子类型点亮。还会有一个音频放大器驱动一个 1W 的小音箱来提供一些音效。太阳能电池板用于为电池充电，电池将为转换器供电，转换器产生 GMT 阵列所需的逻辑和高电压。GMT 信号通过脉冲整形器，然后通过逻辑门，最后被放大以驱动 led 和音频放大器。根据粒子通过 GMT 的方向和顺序，该设备将产生 4 种颜色之一的明亮闪光——红色、绿色、蓝色或白色。它还会触发三个音符的第一个生成，即 C、F、G 或所有三个音符的组合。逻辑部分使用[符合检测](https://en.wikipedia.org/wiki/Coincidence_circuit)，这在他早期的迭代中运行良好。重合检测器是一个“与”逻辑，当两个输入事件在时间上彼此足够接近时，它产生一个输出。他试验了几个设计版本，然后决定采用三个 555 单稳态多谐振荡器来提供初始脉冲整形，随后是一些与门。一个整洁的 PCB 设计将所有这些结合在一起。

虽然原型被安置在木箱中，但他将尝试各种外壳和安装选项，看看哪种效果最好——柱灯柱、球体、挂在树上或三脚架上的东西，或者像铺路块一样放在地上的东西。未来的原型和装置可能包括软件、脉冲求和以及固态探测器。下面嵌入的是他当前版本的探测器的视频，但他的项目页面上还有几个有趣的视频值得一看。如果你对此感兴趣，可以看看这本欧洲粒子物理研究所的小册子——[LHC](http://cds.cern.ch/record/2255762/files/CERN-Brochure-2017-002-Eng.pdf)，这是一本简单解释粒子物理学和 LHC 信息的指南。

 [https://www.youtube.com/embed/Y3NwYVvT4wk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Y3NwYVvT4wk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2017](https://hackaday.io/prize) is Sponsored by:[![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Texas Instruments](img/3734f1c96ffff85ea2a7eaddc92844ba.png)](https://hackaday.io/ti)