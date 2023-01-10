# 打造您自己的数字面板仪表

> 原文：<https://hackaday.com/2017/12/02/build-your-own-digital-panel-meter/>

从通常的进口电子模块零售商处购买的一种流行产品是数字面板仪表。一笔很少的钱就可以获得一个七段显示屏的模块，你可以把它贴在电源的前面，或者投影出来以便于读取。甚至在这些超廉价的中国产品出现之前，就已经有现成的数字电表了，其生产线可以追溯到 20 世纪 70 年代的 Intersil 7106 等芯片。

[Marcus Taciuc]避开了现成的部件，并且[创造了他自己的数字面板仪表](https://hackaday.io/project/27794-build-your-own-panel-meter)。他使用 MSP430 微处理器作为设备的大脑，前端使用日立 HD44780 兼容的液晶显示器。为 MSP 的 ADC 输入端供电的电阻和运算放大器的适当组合，使得他的电表可用于测量最高 40 VDV 和最高 10A 的电流。

他放了一个视频，我们把它放在了休息时间的下面，展示了这种电表的用途:在看起来像是希斯基特设备的经典部件中替换动圈式电表。一个 3D 打印的支架可以让新的血糖仪适合原来血糖仪的圆孔，LCD 在前面。你可能仍然需要一个预制的仪表模块，但是你不能否认这个看起来不错。

 [https://www.youtube.com/embed/Zpa7TBHG6Ks?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Zpa7TBHG6Ks?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



并非所有的液晶面板仪表都如此完美。几年前，我们用一元店计步器带给你一个[。](https://hackaday.com/2012/11/12/4-volt-meter-from-a-dollar-store-pedometer/)