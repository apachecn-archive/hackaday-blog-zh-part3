# 无线双节棍遥控！

> 原文：<https://hackaday.com/2017/04/10/wireless-nunchuck-rc-remote/>

当他的儿子想要一个新玩具时，[丹]令人钦佩地挺身而出。作为一名敬业的父亲，他没有买新的东西，而是趁机溜到他的工作台，将一个[Wiimote nuncchuck 转换成一个完全无线的控制器](https://trandi.wordpress.com/2017/02/26/rc-car-electronics/),用于他儿子的旧遥控车，这辆车几年前就被拆除并重新组装了。

打开双节棍的包装，把 I2C 线收起来，这一切都很简单。从那里，他结合了一点代码，一个 Arduino pro mini 和两个 1K 欧姆的电阻，以利用一直躺在周围的奥雷尔 RTX-MID 收发器。不浪费，不匮乏。

TI Stellaris Launchpad 是汽车本身的智能，与 TB6612FNG 电机控制器相一致。两台带有 3D 打印齿轮的 Solarbotics GM9 发动机给了这辆车一些急需的乐趣。

 [https://www.youtube.com/embed/telCzXIw5gQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/telCzXIw5gQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



用丹自己谦逊的话来说:“没什么不寻常的，只是一个很好的例子，说明一个人可以用任何黑客房子周围大部分积满灰尘的部件做什么。”如果任何新父母有一个备用的 Wiimote，你可以使用红外发光二极管来制作一个相当有效的婴儿监视器。