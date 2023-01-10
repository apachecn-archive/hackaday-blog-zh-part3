# Hackaday 奖参赛作品:不要建造这个

> 原文：<https://hackaday.com/2017/07/24/hackaday-prize-entry-dont-build-this/>

ESP8266 是一款出色的硬件。我们最初的想法——以及最初的市场宣传——使用 Hayes 调制解调器命令的简单 UART 到 WiFi 桥已经变成了最好的嵌入式平台之一。这是一个强大的小微控制器，它有 WiFi，可以发送原始帧。最后一点很棒，因为它允许一些恶作剧或欢笑，这取决于你的观点。

为了他的 Hackaday 奖参赛作品，[Tejas]正在用 ESP8266 建造一个 WiFi 干扰器。这是一种小型设备，能够断开任何人与无线接入点的连接。你应该建造它吗？不，你能吗？当然，为什么不呢？

这个 WiFi 黑客工具的代码取自 ESP8266 deauth toolkit 的创建者[【spacehuhn】](https://github.com/spacehuhn/esp8266_deauther)，尽管【Tejas】违反了【space huhn】的(非开源)代码的许可。这个神奇的固件使用管理包来发送[认证帧](https://mrncciew.com/2014/10/11/802-11-mgmt-deauth-disassociation-frames/)，有效地允许任何人从 WiFi 路由器上断开任何设备。为什么会有人想这么做？当然是恶作剧，但也有一些技术可以让攻击者获得 WiFi 的密码。

虽然有一些方法可以防止 deauth 攻击，但大多数路由器没有启用管理帧保护。在任何情况下，我们都将在本周的 DEF CON 上看到 deauth 攻击到底有多烦人。聪明的钱花在了一小部分 DEF CON 与会者身上，他们与 ESPs 和 Caesar 的 CTO 在一起，非常非常不高兴。

The [HackadayPrize2017](https://hackaday.io/prize) is Sponsored by:[![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Texas Instruments](img/3734f1c96ffff85ea2a7eaddc92844ba.png)](https://hackaday.io/ti)