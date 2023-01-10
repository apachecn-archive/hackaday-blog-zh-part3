# 创客仓组织者创建创客空间门禁系统

> 原文：<https://hackaday.com/2015/12/13/maker-barn-organizer-creates-makerspace-access-control-system/>

MakerBarn 是伍德兰兹和德克萨斯州汤博尔(休斯顿北部)之间的一个新的创客空间。创始人之一、退休设计工程师乔治·卡尔森(George Carlson)希望确保只有通过机器认证的会员才能使用它。他与[Kolja Windeler]合作创建了 MACS 或 Makerspace 访问控制系统。他有一个解释 MAC 电脑的视频，休息之后，另一个解释该系统基于浏览器的用户界面。

一个控制盒，[乔治]称之为工作站，控制机器的电源。会员徽章上有一个 RFID 标签，当插入车站的阅读器时可以被读取。如果成员被授权使用机器，则电源被启用。为了安全起见，会员的徽章必须留在读卡器中以保持电量。阅读器使用 Particle 的光子板，通过 WiFi 链接到 Raspberry Pi 服务器。

[Kolja]开发了一个 Pi 系统来维护会员号码和他们可以使用的机器的数据库。该列表被定期或在更新发生时发送到电台。用户界面是基于制造商局域网的浏览器，因此可以通过空间中的计算机或智能手机进行维护。目前已经制造了 21 个 MACS 模块，其中一些将被送往德国汉诺威大学作为他们的汽车爱好商店。

[乔治]不仅领导了 MAC 电脑的研发工作，而且是在一个杆仓内完成建造，使 MakerBarn 成为现实的关键人物。

 [https://www.youtube.com/embed/zLidqAPo3Cs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/zLidqAPo3Cs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

