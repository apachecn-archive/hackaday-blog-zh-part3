# 用 ESP8266 窃听

> 原文：<https://hackaday.com/2017/11/02/eavesdropping-with-an-esp8266/>

在过去，间谍使用模拟无线电窃听器窃听对方。如今，一切都在云端。[黑客海狸]的[Sebastian]想知道他是否能做一个小而便宜的 WiFi 窃听器。进入 ESP8266 和[一些编程奇才](http://hackingbeaver.com/?p=957)。

[Sebastian]正在使用 NodeMCU，但表示它可以缩减到任何 ESP8266 板，对其余电子设备进行类似的削减，但这只是一个概念验证。PIC 18 MCU 以 8 位分辨率对来自麦克风的 10 kHz 音频数据进行采样，并将其存入 512 字节的缓冲区。一旦填满，GPIO 引脚被拉下，ESP8266 通过 WiFi 将数据发送到等待的 TCP 服务器，该服务器会实时录制或播放音频。

[Sebastian]计算出他至少需要 51.2 毫秒来传输数据，这种设置很容易处理，但偶尔会有两到三秒的意外故障。为了解决这个问题和其他问题，[Sebastian]让 ESP8266 控制 PIC 的 reset 引脚，以便两者始终保持同步。

主要障碍是在 ESP8266 上使用 SPI 每当 PIC 试图传递 512 字节的数据时，ESP 就会复位！经过多次不同的尝试后，[Sebastian]的解决方案是 bitbang SPI，减慢传输速度，但不会崩溃。结果！我们想知道在通过 WiFi 发送之前，他可以通过一点数据压缩将这一点推进多远。

 [https://www.youtube.com/embed/bxUD8CM0LWY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/bxUD8CM0LWY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



现在唯一的问题是，你是否需要因为害怕被监听而开始砸碎附近的任何[扬声器](https://hackaday.com/2016/12/18/eavesdropping-via-headphones/)。即使你做到了，还是有一些[老派的方法](https://hackaday.com/2016/08/12/hacking-when-it-counts-spy-radios/)来保持警惕。