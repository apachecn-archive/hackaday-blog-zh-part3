# 路由器 Rebooter 消除麻烦

> 原文：<https://hackaday.com/2018/01/31/router-rebooter-eliminates-hassles/>

一些低端或老式的路由器可能会在你的房子或公寓里获得一个不错的 WiFi 网络，但这些廉价制造的设备经常受到微妙的软件问题的困扰，导致路由器本身在运行几天后变得没有反应。一个解决方案是，只要互联网消失，就手动重启路由器，但更好的解决方案是[为你建立一个这样的东西](https://www.youtube.com/watch?v=hbA4t5nBcB0&feature=youtu.be)。

[Charlie]作为家中事实上的 IT 人员，遇到了这个问题，他不想为这样一个简单的问题而烦恼。他的解决方案包括一个继电器、一个 ESP8266 和一个 Wemos D1 mini。该设备通过路由器连接到互联网，偶尔会向另一个地址发送 pings。如果在一段时间后无法成功 ping 通地址，设备会通过激活继电器来重启路由器。

由于这不是最新的想法，如果你经常被路由器问题困扰，有许多方法可以解决这个问题，无论是来自你自己的路由器，还是来自把你当作个人 IT 部门的朋友和家人。一种解决方案根本不涉及任何额外的硬件，只要你的路由器/调制解调器附近已经有一台计算机，其他解决方案解决这个问题[当它发生在调制解调器](https://hackaday.com/2015/08/22/hackaday-prize-entry-netboot-powercycles-your-modem-when-you-cant/)而不是路由器上。

 [https://www.youtube.com/embed/hbA4t5nBcB0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/hbA4t5nBcB0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

