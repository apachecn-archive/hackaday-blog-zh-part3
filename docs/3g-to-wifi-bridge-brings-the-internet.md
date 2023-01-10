# 3G 转 WiFi 桥带来互联网

> 原文：<https://hackaday.com/2017/03/28/3g-to-wifi-bridge-brings-the-internet/>

[AFO NSO]77 岁的祖母住在一个相当偏远的地方，只有 AM/FM 无线电接收，偶尔也有一个失灵的座机将她与世界其他地方连接起来。最近的 3G 手机发射塔在 7 公里之外，用手机也达不到。但是[Afonso]决定让她和远房亲戚进行视频聊天。让奶奶进入全球蜂巢思维的方法？建造一个[定制天线](http://home.oraculo.pt/2017/03/21/diy-2100mhz-3g-yagi-antenna/#more-231)到达发射塔，[使用树莓皮](http://home.oraculo.pt/2017/03/21/3g-wifi-raspberry-pi-gateway/)将其连接到本地 WiFi。

该计划的第一步是确保 3G 长期有效，因此[Afonso]制作了一个花式天线的原型，如上所述，并[在连接器](http://home.oraculo.pt/2017/03/21/thoughts-huawei-crc-9-antenna-connector/)上进行黑客攻击，以将其安装到华为 CRC-9 无线电调制解调器上。这让他获得了一个工作数据连接，它发送了一个不错的 4-6 Mbps，足以保证以后投资一些更好的设备。概念证明，对吧？

在桥接方面，他真的烧穿了一个 WR703N 路由器，然后将一个树莓派放入一个装有各种无线电的防水盒中。剩下的就是配置文件的问题，让`iptables`将 3G 无线电的 PPP 负载转发到 WiFi，等等。当然，他想为她远程管理机器，所以他[为管理留了一个永久的 SSH 后门](http://home.oraculo.pt/2017/03/21/reverse-ssh-tunnel/)。其他运行远程树莓 pi 的人应该看看这个。

我们认为黑客将连接掌握在自己手中是一件很棒的事情。我们已经看到了许多类似的 WiFi T1 的壮举，事实上[Afonso]之前已经用 24 dBi 的相控阵天线走上了这条路。最终，相对简单的 3G Pi-and-Yagi 组合胜出。

项目的第二部分，教他的祖母使用安卓手机，已经在进行中。[Afonso]报道称，在跑步两周之后，她已经有了一个 Instagram 账户。我们称之为成功！