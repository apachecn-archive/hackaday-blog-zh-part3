# 无线网络摄像头，无需繁琐的云服务

> 原文：<https://hackaday.com/2017/12/08/a-wireless-webcam-without-a-cumbersome-cloud-service/>

在一位朋友购买了一台需要使用云服务才能使用的 nannycam 后，马丁·卡雷尔(Martin Caarels)心想——正如他所说的那样——“我或许可以用树莓派来做这件事！

总之，[Caarels]收集了一个 4000 毫安时的电池，一个带有微型 SD 卡的 Raspberry Pi 3，一个罗技 c270 网络摄像头，以及将这个项目结合在一起的关键组件:一个橡皮筋。一旦他在 SD 卡上下载并设置了 Raspbian Stretch Lite，他就将它插入 Pi 并通过电缆连接到网络。从那里，他必须 ssh 到 Pi 来获取它的 IP，这样他就可以让它跳到 WiFi 上。

现在他实际上已经有了一个无线网络摄像头，是时候把它变成一个合适的安全摄像头了。

不是反高潮，但所有[Caarels]必须做的就是安装运动——一个运动检测软件——配置一些设置，并设置它在启动时作为守护程序运行。从那里，这是一个简单的情况下访问端口 8080，而在他的家庭网络。如果这看起来很简单，那么这意味着你已经拥有了自己做这个项目的技能——去做吧！

如果您也想放弃任何婴儿监控软件的繁琐服务，[我们已经为您提供了](https://hackaday.com/2017/10/21/fruitnanny-the-raspberry-pi-baby-monitor-for-geeks/)。