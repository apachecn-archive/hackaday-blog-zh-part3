# ESP 到 Wireshark

> 原文：<https://hackaday.com/2017/07/06/esp-to-wireshark/>

大家最喜欢的数据包嗅探工具 Wireshark 已经问世近二十年了。这是可用的最流行的网络分析工具之一，部分原因是它是免费和开源的。它的受欢迎程度保证了它最终将与无线硬件世界的后起之秀 ESP32/8266 配对，[spacehuhn]最终将这两个工具结合在一起，以嗅探 WiFi 数据包。

[spacehuhn]创建的库使用 ESP 芯片将 Pcap 文件(默认的 [Wireshark](https://www.wireshark.org/) 文件类型)保存到 SD 卡上，或者通过串行连接发送数据。该程序每 30 秒运行一次，每次创建一个新的 Pcap 文件。对于您可能使用的各种硬件，有许多示例脚本，因为这是为 ESP 平台编写的，所以它也是 Arduino 兼容的。[spacehuhn]已经把它写成了一个概念验证，所以仍然有一些粗糙的边缘，但是它看起来非常有希望成为一个网络分析工具。

[spacehuhn]对无线网络也不陌生。他的 YouTube 频道充满了他探索各种漏洞和测试其他硬件的有趣视频。他以前也曾因使用 [ESP8266 作为 WiFi 干扰器](http://hackaday.com/2017/03/30/sir-it-appears-weve-been-jammed/)而被报道过。

 [https://www.youtube.com/embed/3Ac6X6ZBQ0g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/3Ac6X6ZBQ0g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

