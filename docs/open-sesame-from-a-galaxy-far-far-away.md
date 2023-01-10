# 芝麻开门，来自一个遥远的星系。

> 原文：<https://hackaday.com/2016/02/14/open-sesame-from-a-galaxy-far-far-away/>

[TVMiller]对他的项目的描述是史诗般的，值得逐字复制粘贴(这是我们的读者经常称赞我们的)。用他自己的话说，“在我的酒柜里发现了几个备用的 Midichlorians，我训练并使用它们来打开一扇笨重的大门。原力运动穿过我的内心，由 Pebble Classic 加速计转换，触发发送到(粒子)云(城市)的命令，该命令返回到粒子光子，触发 TIP120 触发现有 RF 收发器上的按钮。愿可笑的手势与你同在，永远。”就这样，[门绝地](https://hackaday.io/project/9528-gate-jedi)诞生了，你将需要 47 个迷地龙，以及一些其他琐碎的零件来建造一个。

Pebble 手表连接到他的 android 智能手机。一个 [Pebble ~~(android)~~ 应用](https://hackaday.io/project/9528-gate-jedi/log/31409-pebblejs-app)将加速度计数据发送到 Particle(之前称为 Spark)云服务。从那里，数据被推送到光子物联网板，该板运行[几行代码](https://hackaday.io/project/9528-gate-jedi/log/31408-photon-code)。光子的输出打开 TIP120 功率晶体管，进而触发现有的 RF 传输接收器打开门。

这看起来比轻型军刀更酷。看看他召唤原力的视频。如果你想做更多的事情，尝试将手势控制与这个 [Pebble Watch hack 集成，将其变成一个家庭自动化控制器](http://hackaday.com/2013/05/03/pebble-watch-hack-makes-it-a-home-automation-controller/)。

 [https://www.youtube.com/embed/my1ruKJRsX4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/my1ruKJRsX4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

