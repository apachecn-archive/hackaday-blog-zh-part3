# Hackaday 奖半决赛:机器人定位服务

> 原文：<https://hackaday.com/2015/09/24/hackaday-prize-semifinalist-location-services-for-robots/>

未来的机器人将呆在家里，并准备好做我们让它们做的任何工作。但是他们需要知道他们在房子里的位置。利用加速度计和陀螺仪进行航位推算正好是一个足够的解决方案；我们真正需要的是室内定位服务。对于他的 Hackaday 奖参赛作品，[戈兰]就是这样做的。他正在建造一个小装置，可以在室内以 10 厘米的精度找到自己的位置。

[gran]的 LPS Mini 是围绕一个非常有趣的部分构建的 Decawave DWM100。这是一个模块，它使用 802.15 无线电来测量从几个“锚”到标签的距离。这本身就为 LPS Mini 提供了 10 厘米精度的导航系统。利用 IMU 收集加速度计、陀螺仪和罗盘数据，甚至利用微型高度计，可以实现更高的精度。结果是一个知道自己确切位置的小板子。

就实际用途而言，这些 LPS 迷你板被用来在伦敦海沃德画廊的艺术展上移动床。虽然在艺术画廊中移动床听起来不像是一项改变游戏规则的发明，但想想 GPS 在 20 世纪 80 年代的用途——没有人能想象出一种芯片能告诉你你在哪里，或者能让四轴飞行器保持正确的航向。

你可以看看下面[戈兰]的 LPS 迷你视频。

#### 2015 年[黑客日奖](http://hackaday.io/prize)由以下机构赞助:

[![](img/8e6c49d55ea91b307d7d191b75ab18c8.png)](http://hackaday.io/atmel)[![](img/6b53a13e67e0346985e237ef126c1bcc.png)](http://hackaday.io/freescale)[![](img/3fe105965ef22414d89f71032d9babee.png)](http://hackaday.io/microchip)[![](img/ebcbe4e97993de26ebcf849e70523a14.png)](http://hackaday.io/mouser)[![](img/15f4f8aaed16b020832d8be6282e47f5.png)](http://hackaday.io/ti)

 [https://www.youtube.com/embed/KBwRA4_oRe0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/KBwRA4_oRe0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

