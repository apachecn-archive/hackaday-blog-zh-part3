# XLIDAR 是一个旋转木马式的飞行时间传感器

> 原文：<https://hackaday.com/2018/06/29/xlidar-is-a-merry-go-round-of-time-of-flight-sensors/>

[JRodrigo]的 [xLIDAR 项目](https://hackaday.io/project/100965)是那些看起来非常吸引人的可行想法之一，它直接进入 PCB 原型，中途没有做太多停留。这个概念是将三个面向外的 VL53L0X 距离传感器安装到一个小 PCB 盘上，然后用电机和皮带转动该盘，同时读取读数。当传感器转动时，它们的距离读数可以用于描绘周围环境的图片(至少在大约 1 米内，这是 VL53L0X 的最大范围。)

硬件被设计成可访问的，并且具有“所见即所得”的强烈元素距离传感器位于小型分线板上，该板通过 DC 电机和 3D 打印皮带驱动来转动传感器盘。即使是编码磁盘移动和零位置的方法也具有相同的所见即所得直白性:传感器磁盘底部的弹簧触点和中断的裸铜迹线充当物理开关。事实上，同心圆图案的裸露铜迹线和从 SD 卡插座中取出的弹簧针是在磁盘转动时提供电力和通信的。

原型看起来很好，听起来应该可以工作，但它的表现如何呢？一旦[罗德里戈]做了一些测试，我们就会知道了。在那之前，如果有人想尝试自己的方法而不是从零开始，电路板设计可以在该项目的 [GitHub 库](https://github.com/JRodrigoTech/xLIDAR)上获得。

The [HackadayPrize2018](https://hackaday.io/prize) is Sponsored by: [![Microchip](img/20eb9d92b47da4c15177567c02a65727.png)](https://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey)  [![Supplyframe](img/2d012d9fc9c7873688699aeadb4742d2.png)](https://supplyframe.com/)