# 中等价位的硬件开始重视软件无线电

> 原文：<https://hackaday.com/2015/09/25/mid-price-hardware-gets-serious-about-software-defined-radio/>

普通黑客读者习惯于看到将廉价的 USB 电视加密狗用作软件定义无线电(SDR)的黑客。有很多软件可以和他们一起工作，包括优秀的 GNU Radio 软件。然而，硬件非常简单。没有修改，USB 加密狗不会得到更低的频率。

有很多其他 SDR 收音机可用，但它们的价格要高得多。但是我们最近注意到了 RSP 的 SDRPlay，他们现在已经在美国发行了。制造商表示，它将接收 12 位分辨率的信号，频率范围为 100 kHz 至 2 GHz，带宽为 8MHz。USB 电缆为电脑提供电源和连接。最精彩的部分？一个支持 Windows、Linux、Mac、Android 的开放 API，甚至可以在 Raspberry Pi 上运行(并且[也有 GNU Radio 支持](http://www.sdrplay.com/platforms.html))。

如果你像我们一样，你的大脑已经在思考你可以用一个相当便宜(大约 150 美元)的接收器进行黑客攻击。当然，你可以把它仅仅作为一个接收器，但是它可以做更多的事情。例如，下面的第二个视频显示了一个使用该设备作为 panadapter 的 ham(一个相当于频谱分析仪的 ham 工具，可以直观地监控整个 ham 无线电波段的活动)。

该器件有八种不同的前端滤波器，可根据您选择的频率进行选择。我们还没有机会尝试一个(敬请期待)，但[规格看起来令人印象深刻](http://sdrplay.com/docs/SDRplay_Technical_Information_r1p4.pdf)——尤其是价格。当你想到我们已经看到廉价的 SDR 制造[测试设备](http://hackaday.com/2015/03/14/measuring-filters-and-vswr-with-rtl-sdr/)甚至[无源雷达](http://hackaday.com/2015/06/05/building-your-own-sdr-based-passive-radar-on-a-shoestring/)时，你只能想象社区会用这些盒子梦想出什么。

 [https://www.youtube.com/embed/U3qvjjpzsQQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/U3qvjjpzsQQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/fDq_0BCgpdE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/fDq_0BCgpdE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

