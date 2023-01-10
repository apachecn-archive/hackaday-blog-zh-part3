# 深度灵活寻呼协议

> 原文：<https://hackaday.com/2017/08/12/flex-pager-protocol-in-depth/>

我们喜欢寻呼机黑客。我们最早的一个傻瓜完全逆向工程了一个餐馆寻呼机的协议，结果发现它是行业标准的 POCSAG。多。

[玉米]显然抓到了同样的痒处，但在荷兰，FLEX 协议更为普遍。除了带我们了解 FLEX 系统的所有细节之外，他还买了一个 FLEX 寻呼机，把它拆了，然后把 T2 焊接到 ATMega328 电路板和 ESP8266 上。前者进行 FLEX 解码，后者在他的本地网络上发布听到的任何内容。

如今，我们确信你可以用 [Raspberry Pi 和 SDR](http://hackaday.com/2013/06/18/pager-message-sniffing-with-rpi-and-sdr/) 做同样的事情，但我们喜欢购买寻呼机并接入其信号的老派方法。它是一款更好的独立设备，功耗预算低得多。如果你发现自己拥有一些旧的 POCSAG 寻呼机，你应该看看[Corn]以前的工作:[一个发送页面的 OpenWRT 路由器](http://hackaday.com/2014/12/30/bringing-a-legacy-pager-network-back-to-life/)。