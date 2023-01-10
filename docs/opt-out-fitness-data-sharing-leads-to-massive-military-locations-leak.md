# 选择退出健身数据共享导致大规模军事地点泄漏

> 原文：<https://hackaday.com/2018/01/28/opt-out-fitness-data-sharing-leads-to-massive-military-locations-leak/>

使用健身追踪器锻炼的人有他们锻炼的数字记录。他们这样做有各种各样的原因，从收集严肃的医学数据到仅仅满足好奇心。当健身数据包括 GPS 坐标时，它会引发个人隐私问题。但是，即使删除了个人数据，这些数据仍然足以提供足够的信息来泄露世界各地秘密设施的秘密。

Strava 是一种健身跟踪服务，它从几个不同品牌的健身跟踪器中收集数据——想想 Fitbit。它为运动员提供了围绕他们的健身数据建立的社交媒体体验:根据个人目标跟踪进展，并挑战朋友们保持彼此健康。正如拥有个人数据的公司所期望的那样，他们的隐私政策承诺对个人数据保密。在同一隐私政策中，他们还保留了以“聚合和去标识”形式使用用户共享数据的权利，这是社交媒体公司的常见做法。其中一个用途是将所有用户的 GPS 数据绘制成全球热图。这些可视化使用了超过 6 万亿个数据点，可以汇编成一个[迷人的画廊](https://blog.strava.com/galleries/heatmap/)，但也有不好的一面。

过去的这个周末，[Nathan Ruser] [在 Twitter](https://twitter.com/Nrg8000/status/957318498102865920) 上宣布，Strava 的热图还设法突出了世界各地军事/情报人员的演习活动，包括一些可疑但未宣布的设施。更令人担忧的是，一些地图路径暗示着巡逻和补给路线，知识安全官员不希望与整个世界共享。

这是一个非同寻常的错误，非常简洁地说明了物联网的愚蠢。Strava 的匿名化数据共享阻碍了个人，但未能对个人群体做到同样的事情…例如注重健身的现役军人，他们的锻炼习惯在这些热图上有明确的定义。造成这种情况的最大原因(除了一般佩戴跟踪设备之外)是数据共享在默认情况下是启用的，必须退出:

> “您可以通过取消选中此部分的复选框，选择不向 Strava Metro 和热图提供您的匿名公共活动数据。”— [Strava 博客，2017 年 7 月](https://blog.strava.com/privacy-14288/)

我们已经看到[个人健身追踪器被黑](https://hackaday.com/2017/12/29/34c3-fitbit-sniffing-and-firmware-hacking/)，我们之前也看到过[的人通过受控域进行追踪](https://hackaday.com/2017/03/30/creepy-tracking-at-the-house-of-mouse/)，但是【内森】的发现的全球范围使其处于一个完全不同的类别。

[via [华盛顿邮报](https://www.washingtonpost.com/world/a-map-showing-the-users-of-fitness-devices-lets-the-world-see-where-us-soldiers-are-and-what-they-are-doing/2018/01/28/86915662-0441-11e8-aa61-f3391373867e_story.html)