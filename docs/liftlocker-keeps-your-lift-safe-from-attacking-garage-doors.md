# LiftLocker 保护您的电梯安全，防止攻击车库门

> 原文：<https://hackaday.com/2017/02/02/liftlocker-keeps-your-lift-safe-from-attacking-garage-doors/>

汽车升降机曾经是专业机械师专用的工具。然而时代在变。随着价格合理的四柱液压升降机的出现，越来越多的遮荫树技工加入了五英尺高的俱乐部。然而，在家庭车库里安装电梯会带来一些危险。当电梯上有一辆车时，一个家庭远程打开车库门会发生什么？车库门和举升的车辆将会相遇，带来昂贵和/或危险的后果。[乔·奥曼]在一英里外就看到了这个问题。他建造了电梯锁，以确保这种事永远不会发生在他身上。

LiftLocker 的核心是一组开关延长线。两个铸铝盒隐藏了电子设备。一个盒子插在电梯里。另一个盒子插在车库门开启器上。每个盒子包括一个 Sparkfun Redboard Arduino 兼容，一个 RFM22 433 MHz 无线电和一个继电器。输入来自一个安全系统磁性簧片开关。两个盒子在硬件和代码上都是一样的。

操作简单。一个盒子和簧片开关装在电梯上，另一个装在车库门上。如果电梯正在上升，它的簧片开关将会打开。电梯的 Arduino 检测到这一点，并命令其 RFM22 向车库门上的另一个盒子发送信号。收到该信号后，车库门控制器将断开继电器，切断车库门遥控接收器的电源。通信是双向的，所以如果电梯控制器没有听到来自车库门控制器的 ACK 消息，所有的东西都将关闭。点击休息时间，查看系统运行情况。

到目前为止，这一体系运转良好。[Joe]遇到的唯一问题是一些错过的 ACK 信号。我们打赌这是由于无线电模块上方的高电流交流线路的干扰。盒子内部的屏蔽可能会有所帮助。

如果你真的想限制进入你的车库，你可以安装一个[指纹传感器启动的车库开门器](http://hackaday.com/2016/03/16/fingerprint-garage-door-wont-open-every-time-a-neighbor-microwaves-a-burrito/)。你甚至可以黑掉一个 [ESP8266 来记录所有的打开/关闭事件到 Google Drive](http://hackaday.com/2017/01/15/garage-door-opener-logs-to-google-drive/) 。

 [https://www.youtube.com/embed/AbxHpfJ9e18?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/AbxHpfJ9e18?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

