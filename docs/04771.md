# 伺服控制物联网灯开关

> 原文：<https://hackaday.com/2017/01/17/servo-controlled-iot-light-switches/>

物联网玩起来很好玩；有各种各样的设备可以实现自动化和远程控制。不过，这可能是粗略的——在编写自动植物浇水系统时犯了一个错误，你可能会淹没你的房子。在空间加热器上犯了一个错误，你就可能把它烧掉。将这些风险与许多人居住在租赁物业的事实相结合，将物联网引入您的家庭可能是一个困难的命题。

[Suyash]想出了一个解决办法，通过[建造 3D 打印灯开关盖，增加伺服控制](https://github.com/suyashkumar/smart-lights)。这是一个很好的解决方案，它不需要修改任何电源布线，并以正常方式与标准开关接口。这种方式更安全——有市政布线代码是有原因的。这是一个你可以用 3D 打印机做什么的很好的例子，除了打印出尤达头像和钥匙链。

事情的后端由古老的 ESP8266 处理，由[Suyash]的定制物联网库(称为[conduit](https://github.com/suyashkumar/conduit))负责。该库是一种快速构建具有 web 界面的物联网设备的方法，[Suyash]声称使用该工具可以在 5 分钟内从云中闪烁 LED。

关于物联网灯开关的另一个例子，请查看 2016 年的 [Hackaday 奖参赛作品。](http://hackaday.com/2016/09/24/hackaday-prize-entry-theia-iot-light-switch/)