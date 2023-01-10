# espple:ESP8266 上的无线苹果 1

> 原文：<https://hackaday.com/2017/12/30/espple-a-wireless-apple-1-on-an-esp8266/>

苹果 1 是 1977 年突然出现的三大业余爱好者电脑之一。与 2001 年的宠物和 TRS-80 不同，苹果 1 只生产了几百台，而且今天只有少数几台，你必须花大价钱为自己买一台沃兹尼亚克原创的。

当然，Apple 1 的体验很容易被模仿，但[这款 ESP8266 在硬模式下模仿 Apple 1](https://github.com/hrvach/espple)。它的创造者[Hrvoje Cavrak]称之为 Espple，它模仿了基于 6502 的 1 MHz 原件，同时提供了 20kb 的 RAM，这是对 4kb 标准的相当大的升级。完整的原始字符集提供了旧时代的感觉，并有一个基本的解释器准备好了。然而，这里的亮点是模拟器是完全无线的。您通过 telnet 连接到 8266，而不是直接连接键盘，视频通过 GPIO 引脚作为 60 MHz PAL 发射机进行无线传输。你只需要用一小段电线就可以将信号传输到第四频道的模拟 PAL 电视上；下面的视频展示了一点基本的代码运行和低分辨率版本的沃兹本人。

你会在这些地方发现大量的苹果模拟器，从 Arduino Uno 上的苹果电脑到 ESP32 上的微型 Mac 电脑。不过，至少到目前为止，苹果 1 的模拟还不多。

 [https://www.youtube.com/embed/rCqbB1UmW8o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/rCqbB1UmW8o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

