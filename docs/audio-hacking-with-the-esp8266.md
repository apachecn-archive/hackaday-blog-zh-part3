# 使用 ESP8266 进行音频黑客攻击

> 原文：<https://hackaday.com/2018/04/12/audio-hacking-with-the-esp8266/>

如果您研究支持 WiFi 的 ESP8266 微控制器的规格，您会注意到它具有一个 I2S 音频接口。这是一个高速串行端口，旨在以标准格式传输 16 位音频数据，起源于 CD 播放器等消费类音频产品。通常会将专用的 DAC 连接到 I2S 接口来产生音频，但[【Jan ost man】的合成器项目](http://blog.dspsynth.eu/audio-hacking-on-the-esp8266/)避开了这种方法，而是用软件来完成这项工作。他的 I2S 接口以与 1 位 DAC 相同的方式推出脉冲密度调制数据流，这意味着产生音频所需的唯一外部元件是一个简单的低通滤波器。他上传了一段 synth 运行的视频，我们把它放在了休息区的下面。

他给我们的例子是一个 Roland 909 鼓机的基本克隆，他用大量的例子带我们看代码，包括 MIDI。他使用的是 Wemos D1 迷你板，但同样的情况可以在许多其他 ESP8266 平台上复制。

我们之前已经多次介绍过[简]的作品，从他的[极简的基于 Atmel 的设备](https://hackaday.com/2016/09/28/808-drum-machine-in-an-attiny-14-pin-chip/)到[小巧但完美成形的完整仪器](https://hackaday.com/2016/12/11/tiny-ts-just-how-small-can-a-playable-synethesiser-get/)。

 [https://www.youtube.com/embed/lSmbs0qtvrMv?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/lSmbs0qtvrMv?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

