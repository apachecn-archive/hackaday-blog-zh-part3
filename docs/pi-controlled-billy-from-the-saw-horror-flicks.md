# 《电锯惊魂》恐怖片里的派控比利

> 原文：<https://hackaday.com/2017/10/26/pi-controlled-billy-from-the-saw-horror-flicks/>

【David0429】做了一个[非常恐怖的树莓派控制木偶](http://www.instructables.com/id/Remote-Controlled-Billy-From-Saw/)。可怕的是，如果你看过《电锯惊魂》电影，在那里一个连环杀手用一个像它一样的东西，叫做比利，与他的受害者交流。如果你没有，那么这是一个非常漂亮的遥控三轮车木偶黑客。

隐藏在前挡泥板下的步进电机通过旋转前轮来移动三轮车。它使用一个小型的 3D 打印轮子来实现这一点，这个轮子连接到电机的轴上，并压在三轮车的轮子上。转向是通过安装在挡泥板上方并连接到转向柱的 3D 打印齿轮来完成的。伺服电机通过另一个齿轮转动那个齿轮。木偶头部的另一个伺服电机会上下移动它的嘴。

所有这些伺服系统和电机都连接到一个 [Adafruit 步进电机帽](https://www.adafruit.com/product/2348)上，该帽叠放在隐藏在座位下的树莓皮上。远程控制是在任何浏览器的网页上完成的。 [Flask python web 框架运行在 Pi](http://www.instructables.com/id/Smooth-Web-Browser-Motor-Control/) 上，既提供网页，又与网页通信以接收命令。

[David0429]花了很大力气把木偶和三轮车做得像电影里的那个。除了切掉三轮车多余的部分并给它上漆，他还在管状框架内铺设了所有的电线，在需要的地方钻孔并磨出洞来。木偶的骨架是由木头、拉链和铰链制成的，但穿上衣服后，它就非常有说服力了。有趣的是，第一部电影中的木偶没有那么复杂，是用纸巾卷和纸糊制成的。下一次[david0429]想做的唯一的事情就是让马达安静下来以获得最大的爬行，并让它开得更快。然而，对隐藏在挡泥板下的驱动系统的需求导致它只能缓慢地工作。我们在想，也许用后轮驱动它，可以同时提供速度和隐形。有人有想法吗？

在任何情况下，正如你在下面的视频中看到的，结果令人毛骨悚然。

 [https://www.youtube.com/embed/9FLnW_hPUcE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/9FLnW_hPUcE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



《电锯惊魂》中的这个遥控木偶让我们想起了机器人流浪汉德克，它在街上游荡时愚弄了大多数人，偶尔还会用风琴演奏几个音符。有时[机器人被藏在一个看起来无害的填充泰迪熊](https://hackaday.com/2014/10/16/robotic-terminator-teddy-will-protect-you-while-you-sleep/)里，当它移动时看起来非常有活力。