# Litar:使用激光雷达的空气吉他

> 原文：<https://hackaday.com/2018/04/25/litar-an-air-guitar-using-lidar/>

今年，[Blecky]的 Hackaday 奖参赛作品是[一把空气吉他，它使用多个激光雷达传感器来创建虚拟琴弦](https://hackaday.io/project/87794-litar-lidar-air-guitar)。同样有趣的是，他使用了自己的激光雷达传感器， [MappyDot Plus](https://hackaday.io/project/25571-mappydot/log/106150-mappydot-plus) ，这是他 2017 年获奖作品 [MappyDot](https://hackaday.com/2017/08/21/hackaday-prize-entry-mappydot-a-micro-smart-lidar-sensor/) 的增强版本。

他使用六个传感器的巧妙排列来获得四个虚拟字符串。每个传感器扫描 25 度的视野。三个相邻的传感器被用来定义一个串，该串在那些传感器的外部两个的重叠部分中。中间的传感器用于距离数据。

对于和弦，他开始使用一些商业制造的操纵杆，但遇到了一些人体工程学的问题。此外，制造商停止了该产品，这对于一个开源项目来说是不允许的。所以他放弃了这种方法，设计了自己的按钮。他想出了一个 PCB，上面有一个线性霍尔效应传感器和一些弹簧。按钮下面有一块磁铁，位于弹簧上。这样，他可以得到压力，也可以做颤音。

他计划使用蓝牙 MIDI，这样你就可以在手机或笔记本电脑上播放声音，但现在，当你按下琴弦时，他会点亮每个传感器旁边的 LED。

The [HackadayPrize2018](https://hackaday.io/prize) is Sponsored by: [![Microchip](img/20eb9d92b47da4c15177567c02a65727.png)](https://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey)  [![Supplyframe](img/2d012d9fc9c7873688699aeadb4742d2.png)](https://supplyframe.com/)