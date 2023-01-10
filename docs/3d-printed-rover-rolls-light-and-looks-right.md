# 3D 打印的漫游者滚动轻，看起来不错

> 原文：<https://hackaday.com/2017/06/24/3d-printed-rover-rolls-light-and-looks-right/>

[里克·温斯科特]的 RO-V 遥控潜水器 instructable 向你展示如何制作这个看起来很酷、功能强大的机器人。漫游者是 1/10 比例的 truggy，其底盘印有银色和黑色 PLA。它的背面安装了一个无线路由器，前面的双伺服万向节中有一个网络摄像头。[Rick]用 3D 打印零件和他自己敲打的黄铜 M3 螺纹杆制作了自己的转向齿条和齿轮。

简化的驱动系统取消了前、后和中央差速器，从而节省了[Rick]的打印时间、复杂性和重量——他能够包括第二个 4000 mAH 电池。TReX Jr 电机控制器运行一对 Pololu 齿轮电机。所有这些都是由一个 Beaglebone Black 以及一个 Spektrum DX6i 2.4Ghz 发射机和一个 OrangeRx 6 通道接收机控制的。DX6i [Rick]通常被用作飞机/四轴控制器，但他对其进行了重新配置，以控制火星车——左操纵杆控制方向，右操纵杆(升降舵和副翼)控制网络摄像头伺服系统。

技术问题谈够了。我们认为这辆漫游者的脸很漂亮。这种吸引力在很大程度上要归功于一套大谷野生重击轮(一个完全合理的名字)和令人敬畏的 100 毫米震动，这些震动令人愉快地举起了鞭子。然而，[瑞克]优雅的底盘和银黑配色一点也不吃亏。车轮主要是为了酷的因素，但是——[Rick]建议，如果你计划任何实际的越野极限，更换相对适中的 Pololu 20D 齿轮马达，以支持更高扭矩的型号。如果你对自己制作感兴趣，你可以从 Tinkercad 下载[底盘文件](https://www.tinkercad.com/things/0hwi0YAiuys)或者从 Github 下载[猎兔犬代码](https://github.com/rwinscot/RO-V)。

如果你正在寻找其他无人机项目，请查看我们最近发布的[管道漫游车](http://hackaday.com/2015/11/12/heat-duct-rover-explores-stink-rescues-flashlight/)和[太阳能 wifi 漫游车](http://hackaday.com/2016/08/08/hackaday-prize-entry-solar-wifi-rover-roves-at-night/)。