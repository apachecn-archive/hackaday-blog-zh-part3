# 一种基于开源 FPGAs 的超声波驱动器

> 原文：<https://hackaday.com/2018/05/25/an-ultrasound-driver-with-open-source-fpgas/>

超声成像已经存在几十年了，但是开源超声还没有。虽然有大量项目试图创建开放式超声设备，但大多数都集中在图像处理方面，而不是以每秒数百万次的速度 ping 传感器、倾听回声并通过非常高速的 ADC 运行这一异常困难的问题。

为了进入 Hackaday 奖，[kelu124]正在这样做。[他正在构建一个基于开放硬件](https://hackaday.io/project/28375-un0rick-an-ice40-ultrasound-board)、一个奇特的开源 FPGA 和许多非常困难的信号处理的超声板。它还使用了一些 Rick 和 Morty 的参考资料，所以你知道这将会在互联网上流行起来。

超声系统的设计基于 iCE40 FPGA，这是唯一一款具有开源工具链的 FPGA。除此之外，还有大量 ADC、DAC、脉冲发生器和高压部分来驱动现成的超声头。如果你想知道这个超声板是如何与外界接口的，上面也有一个树莓派的标题，所以这个项目有必要的博客信誉。

[kelu] [已经有了一个可以工作的超声波设备](https://github.com/kelu124/echomods/blob/master/matty/20180224b/Readme.md)能够从它的头部发出脉冲并接收回声。现在它只是几个脉冲，但这是朝着真正的工作超声波机器迈出的重要一步，它是围绕一个合理的开源工具链构建的，不需要花费几只胳膊和腿。

The [HackadayPrize2018](https://hackaday.io/prize) is Sponsored by: [![Microchip](img/20eb9d92b47da4c15177567c02a65727.png)](https://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey)  [![Supplyframe](img/2d012d9fc9c7873688699aeadb4742d2.png)](https://supplyframe.com/)