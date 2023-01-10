# 室内花园？那是 Arduino-licious

> 原文：<https://hackaday.com/2018/01/24/an-indoor-garden-thats-arduino-licious/>

园艺是一项有益的工作，对于园艺高手来说，很容易实现自动化。Hackaday.io 用户[MEGA DAS]以简单为重点，发明了一种自动播种机，提供植物渴望的东西:[水、空气和光线](https://hackaday.io/project/29173-arduino-indoor-garden)。

[MEGA DAS]使用 TE215 湿度传感器来监控植物的干渴程度，使用 DHT11 温度和湿度传感器来检查植物周围的气流，使用 BH1750FVI 光传感器的目的显而易见。为了满足这些需求，一台 12V DC 水泵和一个小型水库将保持一切正常，一对 12V DC 风扇模拟微风，一排白色 led 在需要时补充自然光。

定制板是一个 Arduino Nano 平台，带有一个 ESP01 以实现 WiFi 功能，以及一个蓝牙模块以监控工厂在家或外出时的状态。电压调节器、MOSFETs、电阻器、电容器、保险丝——再小心也不过分——螺旋接头连接器，以及其他一些配套部件构成了电路。种植器由激光切割件制成，有足够的空间来安装各种组件并隐藏其他组件。休息之后你可以看看[MEGA DAS]'教程视频！

 [https://www.youtube.com/embed/YLzc1rwn1eU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/YLzc1rwn1eU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[MEGA DAS]已经将他的 Arduino 代码和手机应用程序提供给任何想要建立自己的代码和应用程序的人下载。组装完成后，无论他身在何处，只要轻点几下手机，就能确保他的植物得到很好的照顾。对于一个七天的建筑来说还不算太寒酸。

对于那些喜欢户外园艺的人来说，这里有一个启动种子发芽过程的方法。即使你把混凝土丛林称为你的家，这并不意味着你不能拥有自己的[机器人农场](https://hackaday.com/2014/10/13/robotic-farms-invade-urban-landscapes/)和[自动化堆肥箱](https://hackaday.com/2016/10/23/amalgamate-is-the-internet-of-compost/)！