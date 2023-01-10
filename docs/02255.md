# 逆向工程你的机器人割草机

> 原文：<https://hackaday.com/2016/05/04/reverse-engineer-your-robot-lawnmower/>

你的家是你的城堡，你是你所看到的一切的国王或女王。你已经从零开始建立了自己的家庭自动化系统。为什么你可能会满足于你的机器人割草机的固件？丹尼尔·威格特也不会，所以在[项目负责人](https://hackaday.io/project/6717-project-landlord)中，他已经开始对它进行逆向工程。

你不能责怪他。Worx Landroid 的控制板使用恩智浦 LPC1768 ARM Cortex-M3，调试引脚标在背面。制造商没有保护闪存。它只是乞求[将其固件抛弃](https://hackaday.io/project/6717-project-landlord/log/27268-finally-started-up-the-project-once-again)。到目前为止，[Daniel]已经成功地将设备[连接上和](https://hackaday.io/project/6717-project-landlord/log/27354-bricked-and-unbricked)断开，并且[已经完全映射了控制器的引脚](https://drive.google.com/a/hackaday.com/file/d/0B98aBL1DeE4uc3hLQUhHa1FXUGs/view)，所以他正在完成控制的路上。

现在，他的 GitHub 上有一个正在运行的[概念验证固件，可以驱动机器稍微转一下，并设置刹车。它是免费运行的，丹尼尔正在寻找其他人加入这个项目。他已经完成了艰难的初始工作，所以进去收获回报吧！只是不要忘记在定制固件之前移除刀片。](https://github.com/Damme/LandLord)

机器人割草机中的定制固件会改变世界吗？大概不会。但是这太棒了，而且肯定会改变那些机器人割草机总是卡在绣球花后面的人的生活。

The [HackadayPrize2016](http://hackaday.io/prize) is Sponsored by: [![Atmel](img/2e52aec37df7a9bb2e83735e78e154fe.png)](http://hackaday.io/atmel)  [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](http://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](http://www.digikey.com/)  [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](http://supplyframe.com/)