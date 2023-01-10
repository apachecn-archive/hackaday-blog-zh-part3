# 逆向工程悬浮滑板电机驱动

> 原文：<https://hackaday.com/2016/06/10/reverse-engineering-hoverboard-motor-drive/>

去年冬天的必备玩具是“悬浮滑板”。我们可能都暗暗希望它们是从*回到未来*系列电影中变成现实的滑板，但更现实的是有点类似于微型赛格威的自动平衡滑板车。似乎每个孩子都想要一个，学校禁止他们，媒体对一些更便宜的型号疯狂报道，这些型号缺乏锂离子电池的保护电路，因此有自我焚化的趋势。

[Drew Dibble]对赛车系列( [PRS](http://www.powerracingseries.org/) )感兴趣，在该系列中，玩具电动汽车被加大马力用于比赛。他四处寻找便宜且功率相对较大的发动机，找到了自动平衡的踏板车，并在 Craigslist 上等待不可避免的废弃品。他最终购买了两台 350W 无刷轮毂电机和所有相关的电机控制电路板、陀螺仪，奇怪的是还有一个蓝牙扬声器。马达控制板从踏板车的控制板接收到一个未知的双线数字信号，所以他开始研究它的协议。[他写的关于他如何做到这一点的文章是逻辑线侦探工作的有趣入门。](http://drewspewsmuse.blogspot.co.uk/2016/06/how-i-hacked-self-balancing-scooter.html)

连接上他的逻辑分析仪，他很快就排除了控制信号是 PWM 的可能性，因为所有的信号都遵循相同的时序。两条线都有数据，所以他能够排除 I2C，因为在这种情况下，一条线会携带一个时钟。因此，他只剩下一条串行线，取 38 微秒的时间间隔，他能够计算出它具有相当不寻常的 26315 BPS 的比特率。每个数据包都有 9 位的倍数，所以他要么有 9 位，要么有 8 位奇偶校验，尝试所有可能的奇偶校验方案都导致奇偶校验错误。因此，该板使用了一个非常不寻常的 9 位非标准比特率串行端口。一些实验把他带到了 Arduino 图书馆，他能够从他的马达中获得一些运动。一些聪明的定时侦探工作以后，他可以使他们随意移动，成功！

他所有的项目代码都在 GitHub 上，包括他的 [9 位软件串行库](https://github.com/addibble/SoftwareSerial9)和一个[电机控制草图](https://github.com/addibble/HoverboardController)。

如果你想要一个真正的*回到未来*悬浮滑板，那么你可能要再等一会儿。我们展示了作为不可复制的漂浮艺术品制作的[复制品](http://hackaday.com/2010/05/29/hoverboard-comes-to-life/)，以及更像个人气垫船的[工作板。](http://hackaday.com/2014/12/12/a-simple-hoverboard-everyone-can-understand/)

 [https://www.youtube.com/embed/Stgjf_x8wHk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Stgjf_x8wHk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

