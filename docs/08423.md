# 手机监控车

> 原文：<https://hackaday.com/2018/01/30/cell-phone-surveillance-car/>

家庭安全系统有许多可行的选择，但在你的房间里观看静态摄像头有什么乐趣呢？真正环顾四周的自由可能是迫使[Varun Kumar]建造一个[安全汽车机器人](https://hackaday.io/project/11893-surveillance-car-controlled-via-dtmf)在他的住处周围行驶并确保一切正常的原因。

以成本效益和 WiFi 或互联网接入为目标的 Android 智能手机为这一构建提供了基础——跳过了对单独蓝牙或 WiFi 模块的需要——并由 Arduino Uno、L298 电机控制器和两个齿轮传动 DC 电机为车轮提供动力。

进一步利用手机的功能，机器人由双音多频音控制。使用 app DTMF 音调发生器并通过 3.5 毫米插孔输出，命令由 MT8870DE DTMF 解码器模块解释。虽然这种控制方法存在一些风险——与许多物联网设备一样——【Kumar】通过在安全汽车接受任何命令之前添加一个 PIN 码，规避了 DTMF 的一个漏洞。

他使用 AirDroid 与 VNC 服务器协同工作，从手机上获取实时视频，并在伺服电机的帮助下，使手机能够左右扫描，以获得更好的外观。[Kumar]笔记本电脑上的 VNC 客户端能够访问视频并发出命令。休息之后，请查看实际情况！

 [https://www.youtube.com/embed/ecWZbtY6rOI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ecWZbtY6rOI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



当然，一旦发现入侵者，采取更积极的措施是可能的，甚至可能用一场[冰雹](https://hackaday.com/2011/09/18/mechatron-industrial-looking-security-bot/)把他们赶走。