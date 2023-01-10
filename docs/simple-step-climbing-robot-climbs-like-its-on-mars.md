# 简单的阶梯攀爬机器人像在火星上一样攀爬

> 原文：<https://hackaday.com/2017/08/12/simple-step-climbing-robot-climbs-like-its-on-mars/>

[纳文·坎巴拉]是一位将大多数人认为复杂的构建变得简单的大师。现在他用一个遥控机器人再次做到了这一点，这个机器人可以很容易地爬上台阶，并在崎岖的地形上扮演角色。器件数量很少，而且很多都是常见的。

使这一切成为可能的悬挂是[摇臂转向架](https://en.wikipedia.org/wiki/Rocker-bogie)。这和我们见过的在火星上漫步的各种[漫游者使用的悬浮系统是一样的。整个框架由 PVC 管和一些连接金属条制成，每个车轮都有自己的 12 伏 DC 发动机。电机控制只需一个将](https://en.wikipedia.org/wiki/Mars_rover) [2.4 GHz 接收器与电机控制器](http://robokits.co.in/control-boards/wireless-robot-controllers/rf-2.4ghz-multi-channel-remote-for-3-dc-motors-5a-drive?zenid=c4dchqait91195gjct0j6k5oo3)结合在一起的模块即可完成。观看下面的视频时，请注意 PVC 上只钻了一个孔来连接，而不是两个孔。在只有一个孔的地方，PVC 的两个部分可以彼此独立地自由旋转。转动机器人是通过向一个方向转动一侧的轮子和向相反方向转动另一侧的轮子来完成的。这被称为差动驱动或坦克驱动，我们之前已经强调过它在[制造仓鼠驱动型 BB-8 机器人](http://hackaday.com/2016/06/24/driving-bb-8-more-than-one-way-to-move-this-bot/)中的应用。

 [https://www.youtube.com/embed/3Zx7tGtwF5g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/3Zx7tGtwF5g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



这个机器人还能做得更简单吗？好吧，这已经过去了将近十年，但是我们之前展示过[这个爬楼梯机器人](http://hackaday.com/2009/07/02/clever-stair-climbing-robot/)，它没有使用摇臂转向架悬挂，但是它确实借用了一些相同的想法来卷起那些楼梯面。