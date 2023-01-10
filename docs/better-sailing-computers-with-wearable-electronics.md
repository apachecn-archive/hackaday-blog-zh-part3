# 用可穿戴电子设备更好地驾驶电脑

> 原文：<https://hackaday.com/2016/03/19/better-sailing-computers-with-wearable-electronics/>

帆船运动——特别是赛船会中的小船——是一项需要很多技巧的爱好。像任何爱好一样，有一些设备和电子产品可以让爱好变得更容易。对于航海，它的战术航海罗盘和 GPS 装置。记住，你可能不想直线航行，这意味着把几十年的经验卸给电子设备。与其花数百美元买一台航海电脑，[布鲁克]认为用树莓派和 Pebble 智能手表来打造自己的机器人水手会是一个更好的主意。

航海计算机所需的传感器是正常的——一个 Ublox GPS 单元、一个磁力计、一个加速度计和一个陀螺仪。在帆船上使用也意味着有一个风速计被扔进了混合物中。这些部件被塞进一个防水的聚碳酸酯场箱，带有一个 USB 电源组电池和一个蓝牙 USB 加密狗。

硬件就位后，[是时候编写软件了](http://blog.mrgibbs.io/bluetooth-low-energy-ble/)。这款设备的用户界面是一个 Pebble 智能手表，这意味着有很多 C#和 Mono 的事情要做。这个设备也是一个帆船数据记录器，这意味着[布鲁克]可以将这个项目与[visual sail](http://blog.mrgibbs.io/visualsail-now-free/)集成，这是他几年前编写的一个桌面应用程序，使用 GPS 数据创建帆船比赛的 3D 回放。

* * *

![Raspberry_Pi_LogoSmall](img/87d7e34f7ac8cc3ae6c8619ad96c149e.png)

树莓派零竞赛由 Hackaday 和 Adafruit 主办。奖品包括 Adafruit 的树莓派零和 Hackaday 商店的礼品卡！
[查看全部词条](https://hackaday.io/submissions/adafruitpizerocontest/list)