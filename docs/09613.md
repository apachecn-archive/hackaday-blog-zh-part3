# 便宜的东西:13 美元一个带 SDR 的路由器

> 原文：<https://hackaday.com/2018/05/30/cheap-stuff-to-hack-a-router-with-an-sdr-for-13/>

消费电子产品的历史上充斥着一开始相对无趣的设备，但一旦少数人弄清楚一切是如何运作的，这些设备就会成为硬件开发的壮观平台。Linksys WRT54G 只是一个路由器，直到有人想出如何在其上安装完整的 Linux 系统。那些 RTL-SDR 加密狗只是为了捕捉空中电视，直到有人意识到它们实际上是一种软件定义的无线电。CueCat 只是网络繁荣时期的营销垃圾，直到……好吧，不管怎样，我们还是买了很多 CueCat。

现在，沃尔玛的货架上摆着一款新设备，正等着一些 Linux 黑客来一试身手。这是 Tzumi MagicTV ，一种可以让你在手机上观看无线电视的设备。里面是什么？它是一个微型封装中的 WiFi 路由器、RTL-SDR 和电池组。最精彩的部分？售价 13 美元，显然沃尔玛只是在吹它们。

目前，还没有太多关于 Tzumi MagicTV 盒子内部发生了什么的细节，但是，关于 RTLSDR subreddit 的讨论已经透露了足够多的信息，让我们对正在发生的事情有了一个很好的了解。MagicTV 内部的路由器是 TP-Link TL-WR703N，与几年前取代 WRT54G 成为黑客路由器之王的 WiFi 路由器完全相同。SDR 芯片与普通电视调谐器之一的 astro meta dv b-T2(T1)相同。除此之外，板上有 TX 和 RX 引脚，SSH 是开放的，没有人知道密码，但在撰写本文时，一些人正在让开膛手约翰工作，试图闯入这个盒子。

打开这个 Linux 盒子的最终目标是什么？嗯，它是一个 WiFi 路由器和一个 SDR，所以如果你想制作自己的 [Flightaware ADS-B 记录器](https://hackaday.com/2015/07/18/tracking-nearly-every-aircraft-with-a-raspberry-pi/)，那可能是在桌子上。当然，你实际上可以将它用于预期目的，并将无线电视下载到你的本地网络，但在从沃尔玛(Walmart)购买了 13 美元的盒子后，这似乎变得很乏味。

谢谢[亚当]的提示！