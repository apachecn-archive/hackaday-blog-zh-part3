# 使用 NeoPixel 日出闹钟叫醒您

> 原文：<https://hackaday.com/2016/08/11/wake-up-with-a-neopixel-sunrise-alarm-clock/>

像我们中的许多人一样，[李]每天早上醒来时脾气暴躁，疲惫不堪。一旦他决定尝试做点什么，他决定用 NeoPixels 制作[一个日出闹钟。在 30 分钟的过程中，时钟以蓝色模式逐一照亮 60 个新像素，以模拟日出。](http://www.instructables.com/id/Arduino-Powered-Sunrise-Alarm-Clock-With-Neopixels/)

该时钟有三种模式:30 分钟日出，模拟时间显示，以及秒计数器，该计数器使用 led 的全 RGB 范围来点亮每一秒。为了简单起见，它在 Arduino Pro Mini 山寨版和 RTC 模块上运行。[Lee]把 NeoPixel 条连成五排，每排八条，这样他就可以用 3×5 的字体显示时间。唯一的其他电子器件是保护 led 的无源器件。

新像素很棒，但供电很快就成了问题。[Lee]算了一下，发现他需要 3.4 A 来驱动一切。他在宜家购买外壳时，发现了一个 3 插座 USB 电源适配器，总输出功率为 3.4。[Lee]通过打开适配器并使用两个并行连接的 USB 端口提供 3.4 A 的 5 V 电压，将他的第一个 Instructable 从初学者提升到了中级水平。[Lee]提供了代码以及复制该版本的详细说明。请务必在休息后观看演示。

我们喜欢在这里建造一个好的时钟，尤其是当他们有闪光灯的时候。对于那些对制造闹钟不感兴趣的人来说，这里有一个用 ESP8266 获取时间和天气数据的单词时钟[。](https://hackaday.com/2016/04/27/slim-and-classy-word-clock-shows-the-weather-too/)

 [https://www.youtube.com/embed/MfSMQKHrTd0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/MfSMQKHrTd0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

