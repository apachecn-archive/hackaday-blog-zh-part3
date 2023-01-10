# ColibriNANO USB SDR 接收器综述

> 原文：<https://hackaday.com/2017/08/08/colibrinano-usb-sdr-receiver-reviewed/>

乍一看，ColibriNANO SDR 看起来像另一种廉价的 SDR 加密狗。但在观看了[Mile Kokotov 的] [评论](https://www.youtube.com/watch?v=PT30XEk0KAI)(见下面的视频)之后，你可以看到它是专门为软件定义的无线电服务而构建的。当[Mile]取下外壳时，你会注意到在典型的廉价加密狗上看不到的重金属机身。当然，低端的 RTL-SDR 在 20 美元左右。ColibriNANO 的价格约为 300 美元，所以你会希望物有所值。

频率范围标称值为 10 kHz 至 55 MHz，但如果使用外部滤波器和前置放大器，则可以达到 500 MHz。除了 14 位 122.88 兆采样/秒模数转换器外，该器件还配有 Altera MAX10 FPGA。

除了不同软件包的接口之外，加密狗还支持远程软件。这个想法是把加密狗和天线放在一个有利的地方(也就是说，高和无线电安静)，然后使用 Raspberry Pi 或类似的计算机通过互联网传输信号。

如果您不想要加密狗，我们可以支持[Lukas'] [从头开始构建](https://hackaday.com/2016/07/28/amazing-sdr-built-by-16-year-old/)。如果您正在寻找更多入门资源，请查看[【Richard Baguley】对 SDR 的看法](https://hackaday.com/2016/05/30/hackaday-dictionary-software-defined-radio-sdr/)。

 [https://www.youtube.com/embed/PT30XEk0KAI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/PT30XEk0KAI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

