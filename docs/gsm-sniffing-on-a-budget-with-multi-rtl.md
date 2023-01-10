# GSM 嗅探多 RTL 的预算

> 原文：<https://hackaday.com/2017/01/30/gsm-sniffing-on-a-budget-with-multi-rtl/>

如果你想窃听 GSM 电话的对话或数据，有足够的钱是值得的，因为你需要监听很宽的频率范围。或者，你可以只使用两个便宜的 RTL-SDR 单元和一些聪明的同步软件。[Piotr Krysik]于 2016 年 8 月在 Camp++展示了他在预算 GSM 黑客攻击方面的工作，[的展示视频](https://www.youtube.com/watch?v=xnXMKRIqkZ4)现在刚刚上线(嵌入下面)。妙语是一种既收听上行链路又收听下行链路的方法。

[Piotr]了解他的 GSM 电话技术，白天研究，晚上破解 GnuRadio GSM 解码器。他的演讲证实了这一点，是对 2007 年至今 GSM 黑客攻击的一个很好的概述。《T2》多 RTL 的动力也来自这部作品。尽管[侵入廉价手机](http://hackaday.com/2010/12/30/gsm-hacking-with-prepaid-phones/)或[使用单个 RTL-SDR](http://hackaday.com/2013/10/22/cracking-gsm-with-rtl-sdr-for-thirty-dollars/) 接收 GSM 信号是可能的，但窃听上行和下行信道仍然遥不可及，因为它需要比廉价 RTL-SDR 更多的带宽。更喜欢*两个*廉价 RTL-SDR 模块的带宽。

让两个 RTL-SDR 模块同相工作就像把一个晶体从一个上拆下来，然后把它装在另一个上一样简单。将两者绝对及时地对齐需要非常巧妙的技巧。原来，在频率切换后，绝对定时被保留，因此两个 RTL-SDR 切换到相同的信道，一起锁定在单个信号上，然后切换回来，一个切换到上行链路频率，另一个切换到下行链路。多 RTL 是一个 GnuRadio 源，为你照顾这一点。嘭！价值数百或数千美元的装备被商品硬件所取代，你可以在任何地方花不到一顿丰盛的晚餐就买到这些东西。这是一个伟大的黑客，和一个伟大的演示。

 [https://www.youtube.com/embed/xnXMKRIqkZ4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/xnXMKRIqkZ4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[dnet]的提示！