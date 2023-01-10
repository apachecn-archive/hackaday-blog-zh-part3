# 黑客日奖半决赛选手:一个移动节点

> 原文：<https://hackaday.com/2015/09/03/hackaday-prize-semifinalist-a-mobile-node/>

未来是物联网，或者说我们被告知如此，随之而来的是对连接到互联网的传感器的需求，这些传感器还可以中继 GPS 和位置数据。[Camilo]的[mobile nodes 就是这么做的](https://hackaday.io/project/7033-mobilenode)。他设计了一种设备，可以监听任何传感器，通过 GSM 或 GPRS 将数据上传到互联网，并将所有数据推送到云端。

MobileNode 是一个带有标准 ATMega32u4 微控制器的小型圆形(7cm) PCB。连接到这个 PCB 的是 GSM/GPRS 和 GPS/GLONASS 模块，用于接收 GPS 信号并将所有数据转发到云端。除此之外，几乎可以添加任何传感器，包括光传感器、PIR 传感器、气体和温度传感器，以及几乎任何可以电子测量的其他传感器。

当然，物联网设备上一堆传感器的最大问题是从互联网上获取数据。为此，[Camilo]设计了一个网络界面，直接在谷歌地图上显示传感器数据。你可以看看下面的项目视频。

#### 2015 年[黑客日奖](http://hackaday.io/prize)由以下机构赞助:

[![](img/8e6c49d55ea91b307d7d191b75ab18c8.png)](http://hackaday.io/atmel)[![](img/6b53a13e67e0346985e237ef126c1bcc.png)](http://hackaday.io/freescale)[![](img/3fe105965ef22414d89f71032d9babee.png)](http://hackaday.io/microchip)[![](img/ebcbe4e97993de26ebcf849e70523a14.png)](http://hackaday.io/mouser)[![](img/15f4f8aaed16b020832d8be6282e47f5.png)](http://hackaday.io/ti)

 [https://www.youtube.com/embed/3IubqbmvRx8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/3IubqbmvRx8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

