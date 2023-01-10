# Hackaday 奖参赛作品:WiFi EPaper

> 原文：<https://hackaday.com/2017/05/22/hackaday-prize-entry-wifi-epaper/>

[弗兰克·巴斯]设计了一个便利贴的电子版本:一个有无线上网功能的太阳能电子纸，盒子里嵌入了磁铁。它基于新的 ESP32，想法是你可以通过智能手机或互联网上的云应用程序更新它，以显示任何你想要的信息。作为一个 ePaper 显示器，功耗大大降低，至少如果你小心使用 ESP32。

最终版本计划每小时轮询一次服务器，以获取新图像进行显示。根据最终尺寸和电池限制，我们猜测它可能会经常轮询。当然，这取决于可用的充电灯，当你在房子里时，充电灯通常会减少。该项目还有 3 个按钮来提供用户输入，可以针对各种操作进行定制，正如[Frank Buss]所指出的:

> 例如，将它安装在你奶奶的冰箱上，她可能不太擅长使用现代互联网连接设备。然后你可以送她生日祝福，或者提醒她日程安排。按钮可以用作反馈渠道，比如确认日期。或者当安装在公共场所时，它可以充当公告板。或者它可以用于现代形式的互联网连接涂鸦或其他艺术项目。可能性是无限的。

这个项目立即让我们想起了几天前我们报道的最近的 [SHA2017 徽章](http://hackaday.com/2017/05/08/the-sha2017-badge-revealed/)，它有更大的显示屏和太阳能电池板，或者是去年的[电子墨水 wifi 显示项目](http://hackaday.com/2016/06/12/an-improved-wifi-connected-e-ink-display/)。

最新版本正在用黑/白/红电子纸显示屏进行测试，正如我们在视频中看到的:

 [https://www.youtube.com/embed/3mhUmatstaY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/3mhUmatstaY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2017](https://hackaday.io/prize) is Sponsored by:[![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Texas Instruments](img/3734f1c96ffff85ea2a7eaddc92844ba.png)](https://hackaday.io/ti)