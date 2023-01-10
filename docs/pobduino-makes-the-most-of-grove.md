# PobDuino 充分利用格罗夫

> 原文：<https://hackaday.com/2017/07/27/pobduino-makes-the-most-of-grove/>

玩具机器人的底盘是由吉恩·诺尔制造的机器人的底座。这款机器人名为 [#PobDuino，在引擎盖下有两块 Arduino 兼容板](https://hackaday.io/project/26009-robot-pobduino)。

首先，一个 Seeeduino Lotus，一个布满十几个 Grove 兼容插座的 Arduino 板。电路板的大小与 UNO 相当，安装时插头从机器人的前面伸出，允许对各种 [Grove 系统](http://wiki.seeed.cc/Grove_System/)模块进行特别实验。与此同时，定制的 ATmega328 板(PobDuino)解释流代码指令，并向机器人的各个部分发送命令:伺服系统由 Adafruit 伺服驱动板控制，DC 电机由格罗夫 I2C 电机驱动器驱动。

我们喜欢定制机器人是多么容易，机器人外部有 Lotus 和 Adafruit 16 通道伺服驱动器。即插即用！

在[Elliot]的[我在连接器动物园的生活](http://hackaday.com/2016/11/09/my-life-in-the-connector-zoo/)中了解更多关于 Grove 兼容插头的信息。