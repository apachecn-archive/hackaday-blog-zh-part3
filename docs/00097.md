# Hackaday 奖半决赛选手:全栈物联网平台

> 原文：<https://hackaday.com/2015/09/15/hackaday-prize-semifinalist-a-full-stack-iot-platform/>

有数以百万计的设备和传感器连接到互联网上，未来十年将会增加数十亿。怎么会有人跟踪所有这些传感器？有了物联网设备平台 analog.io 和 Hackaday 奖的参赛作品。

从物联网中收集数据的问题以前已经解决过了。去年，Sparkfun 发布了基于 [Phant](http://phant.io/) 的[data.sparkfun.com](https://data.sparkfun.com/)，这是一款从物联网收集数据的工具。尽管 Phant 可以收集数据，但它只在带有值和时间戳的整齐的列中收集数据。为了把它变得更加直观，analog.io 诞生了。未来，[卢克]将增加对 [thingspeak](https://thingspeak.com/) 和 [Xively](http://xively.com/) 数据流的支持；整个项目旨在后端不可知，允许任何人从任何东西获取数据，将其存储在任何服务器上，并将其连接到 analog.io 进行可视化和共享。

绘制数据提供了一些有趣的机会，比如当[卢克]发现[他的联网水表](https://hackaday.io/project/4648-analogio-a-full-stack-iot-platform/log/23608-measuring-water-consumption)记录的用水量远远超过[的用水量](https://hackaday.io/project/4648-analogio-a-full-stack-iot-platform/log/24326-an-epic-water-meter-fail)时。花园水管上的一个配件松了，水管开始把水倒在离他地下室墙一英尺远的地上。这是一个游泳池在[卢克]的基础上的水的价值，很容易绘制出来。他现在给 analog.io 增加了一个提醒功能。

绘制数据确实有其自身的问题，比如当传感器发送一个错误的数据点时。【Luke】[把这叫做‘毛刺’](https://hackaday.io/project/4648-analogio-a-full-stack-iot-platform/log/25146-introducing-the-de-burr-filter)，analog.io 可以把这些使数据不可读的小尖峰过滤掉，作为图形。制作一个可用的图表需要做很多工作，而[卢克]正在划掉他所有的 t，点上他所有小写的 j。

虽然 Hackaday 奖的许多参赛作品都是在地面上运行，每个传感器都连接到互联网上，但[Luke]的项目从另一端解决了物联网问题，为每个人提供了一种轻松可视化他们数据的方法。这是一个很棒的 Hackaday 获奖作品，也肯定会对许多其他获奖作品有用。

#### 2015 年[黑客日奖](http://hackaday.io/prize)由以下机构赞助:

[![](img/8e6c49d55ea91b307d7d191b75ab18c8.png)](http://hackaday.io/atmel)[![](img/6b53a13e67e0346985e237ef126c1bcc.png)](http://hackaday.io/freescale)[![](img/3fe105965ef22414d89f71032d9babee.png)](http://hackaday.io/microchip)[![](img/ebcbe4e97993de26ebcf849e70523a14.png)](http://hackaday.io/mouser)[![](img/15f4f8aaed16b020832d8be6282e47f5.png)](http://hackaday.io/ti)