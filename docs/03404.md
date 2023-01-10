# Hackaday 奖参赛作品:BunnyBot 自己帮了大忙

> 原文：<https://hackaday.com/2016/09/02/hackaday-prize-entry-bunnybot-helps-out-all-on-its-own/>

[杰克·乔] [想要一个能在千变万化的商店里方便使用的自主机器人](https://hackaday.io/project/12373-bunnybot)。他不想要一个机器人，他必须照看他。如果他说，“把 100 欧姆的电阻给我拿来”，它就会去找并把它们带给他。

他做了一些迭代，最终以不到 1000 美元的价格构建了一个相当不错的机器人平台。它有一个来自 Neato 机器人吸尘器的[实感](http://hackaday.com/2016/01/23/using-realsense-cameras-with-os-x-and-linux/)相机和[测距仪](http://hackaday.com/2016/06/05/in-soviet-russia-diy-laser-rangefinder-scan-you/)。除了麦克风之外，它的底座上还有一整套额外的传感器，这是一家韩国制造商生产的机器人真空吸尘器。更多的组件组合在一起，给它一只手臂和一个抓手。

这个想法是在 Nvidia Jetson TK1 板上完成的。集成显卡上的内核用于执行更快的计算机视觉计算。软件都是基于 ROS 的。

在休息后的视频中可以看到。该机器人使用 SLAM 技术成功导航并完成任务，如取电阻、取水等。[杰克·乔]对他的机器人很满意，我们也会很满意。

 [https://www.youtube.com/embed/GF1XzZ7reig?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/GF1XzZ7reig?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2016](https://hackaday.io/prize) is Sponsored by:[![Atmel](img/2e52aec37df7a9bb2e83735e78e154fe.png)](https://hackaday.io/atmel) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://www.digikey.com/) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/)