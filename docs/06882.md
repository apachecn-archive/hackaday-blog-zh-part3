# 嗅你的本地 LoRa 包

> 原文：<https://hackaday.com/2017/08/22/sniff-your-local-lora-packets/>

随着免许可频谱中的 LoRa 低带宽联网技术在物联网狂潮中获得牵引力，LoRa 网络开始出现在各种意想不到的地方。有时它们是开放的网络，如物联网，有时它们是商业可用的网络，当然，还有完全私有的 LoRa 装置。

如果你对在一个特定的网站上使用 LoRa 感兴趣，这是一个有趣的练习来找出已经存在的 LoRa 流量，为此[Joe Broxson] [已经组装了一个有用的小设备](https://github.com/ImprobableStudios/Feather_TFT_LoRa_Sniffer)。硬件方面，它是一个 Adafruit Cortex M0 羽毛，带有板载 LoRa 模块，与 TFT 羽毛翼配对显示，软件方面，它扫描一组可用的频率，并将找到的任何数据包发送到滚动显示。它还具有将数据包详细记录到 SD 卡中以便以后分析的简洁功能。整体封装在 Adafruit 设计的 3D 打印盒中，是一个非常有吸引力的独立单元。

我们在这里展示了相当多的 LoRa 项目，包括[这个在远程显示中带有 Raspberry Pi 计算模块](http://hackaday.com/2017/02/08/lorawan-and-raspberry-pi-compute-module-for-a-remote-display/)的项目。在劳拉测试意义上更相关的是[这次劳拉测试](http://hackaday.com/2017/04/29/simple-range-testing-for-lora-modules/)。