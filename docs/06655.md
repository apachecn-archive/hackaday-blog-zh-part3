# 走向数字化:升级船只的模拟仪表

> 原文：<https://hackaday.com/2017/08/01/going-digital-upgrading-a-boats-analog-gauge/>

很可能你们中的很多人都没有一艘可以随意摆弄的船。[MAV romancy]最近获得了一个——令他非常惊愕的——模拟仪表。所以为了让他的船保持船形，他给自己造了一个[定制的数字测量仪](http://www.mavromatic.com/2017/07/part-i-custom-nmea-2000-2-round-lcd-multifunction-display-for-boat-gauge/)来监控他的船的数据。

局限于他的船舵上两英寸的洞，在网上搜索显示器发现了一个来自 4D 系统公司的 1.38 英寸的液晶显示器。鉴于空间有限，Teensy 3.2 被证明足够小巧，可以与定制电路板一起放在有限的空间内——后者包括一些备用电路，如果[MAV roxac]想要恢复模拟仪表的话。

他花了两天时间适应显示器的 IDE，当零件到达时，他已经有足够的代码来制作一个功能显示器。

屏幕被安置在一个需要小心闯入的空白计量器中，并且——天才的一击 chrome rim 被证明是一个偶然的电容传感器，只需轻点边框，它就可以在各种信息屏幕之间交换。

 [https://www.youtube.com/embed/oPjjU-vdfA8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/oPjjU-vdfA8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[MAV romancy]最初想安装一个探鱼仪和绘图仪，也可以显示他想要的发动机数据，但事实证明这很复杂，是一个徒劳的麻烦。自然地，他的制造者癖好使得设计一个定制的计量器来显示他想从船的 NEMA 2000 网格中得到的东西成为更鼓舞人心的项目。

你也喜欢在禁航海域航行，但却不能在新船上花钱吗？你可以从建造一艘私人船只开始——有时除了[的微薄收入之外什么都不用。](http://hackaday.com/2014/05/22/home-depot-brand-boat-costs-29-18/)