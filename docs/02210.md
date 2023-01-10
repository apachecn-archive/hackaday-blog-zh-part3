# 开源铅测试仪

> 原文：<https://hackaday.com/2016/05/03/an-open-source-lead-tester/>

如果你曾经需要一个政府行为者的巨大失败的例子，你只需要看看弗林特，密歇根州的水危机。在弗林特市将供水从底特律改为弗林特河后，市政官员未能添加正确的缓蚀剂。这意味着铅溶解在水中，数以千计的儿童接触到饮用水中的铅，政府掩盖真相的行为随之而来，[艾琳·布罗克维奇]出现了，弗林特水厂的工头被发现死亡，存放水记录的市政厅办公室被闯入。

也许是受到了 Flint 的启发，[Matthew]正在开发一款开源的 Lead Tester [，以便参加 2016 年的 Hackaday 奖](https://hackaday.io/project/10438-ospb-an-open-source-lead-tester)。

【马修】的测铅仪不直接测水。相反，它使用光电二极管和 RGB LED 来观察铅试纸的颜色。这些结果被记录下来，通过一点软件后台，只用几台这样的设备，几天之内就可以绘制出整个城市的铅污染地图。

[Matthew]遇到的一个问题是，Pi 没有模数转换，这使得读取光电二极管比仅仅将单个器件插入引脚接头并观察模拟值的上升和下降要困难一些。这真的不是问题，ADC 很便宜，尤其是当你只需要一个低分辨率的单通道模拟输入时。[Matthew]还在考虑使用 Pi 网络摄像头来测量铅试纸。有很多决定要做，但是这个项目出来的任何功能设备在正常运作的政府中都非常有用。希望密歇根州的弗林特也是如此。

The [HackadayPrize2016](http://hackaday.io/prize) is Sponsored by: [![Atmel](img/2e52aec37df7a9bb2e83735e78e154fe.png)](http://hackaday.io/atmel)  [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](http://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](http://www.digikey.com/)  [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](http://supplyframe.com/)