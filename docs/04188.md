# 用 SDR 构建劳拉 PHY

> 原文：<https://hackaday.com/2016/11/18/building-a-lora-phy-with-sdr/>

当它是你的烤面包机时，物联网是可怕的。当你有成百上千个传感器每天将数据发送回基站时，真正的乐趣就来了。这需要低功耗，这意味着低功耗广域网。

LPWAN 有很多选择，但没有几个是完美的。LoRa 是一个罕见的例外，它可以在一个 AA 电池上运行数年，并且范围以英里计。LoRa 的第二层和第三层可以作为公共文档获得，但直到现在，第一层已经获得专利和专有。在 GNU 无线电会议上，【Matt Knight】[发表了一篇关于用软件无线电对](https://www.youtube.com/watch?v=-YNMRZC6v1s&feature=youtu.be)劳拉·PHY 进行逆向工程的演讲。现在，LoRa 对所有人开放，任何人都可以解码这些微小的低功耗设备发出的啁啾声。

GNU 无线电会议上展示的工作建立在今年 [DEF CON wireless village](https://www.youtube.com/watch?v=DmaODrtZgzM) 的早期演讲的基础上。不过，这一次，劳拉 open 有了一个完整的开源解决方案。实验装置由一个[微芯片 RN2903 模块](http://www.microchip.com/wwwproducts/en/RN2903)和一个 Ettus B210 SDR、Python、GNURadio 和 Baudline 组成。最终的结果是[一个 GNU 无线电模块实现了](https://github.com/BastilleResearch/gr-lora)劳拉 PHY。

直到现在，LoRa 的 MAC 和网络层都是完全开放的。然而，PHY 关闭了。芯片制造商似乎喜欢卖芯片。现在，只配备了一个 SDR，就可以读取 LoRa 芯片，监听它们在做什么，并揭示物联网最有趣的一点。