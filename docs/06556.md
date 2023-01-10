# 对着灯说话

> 原文：<https://hackaday.com/2017/07/22/talking-to-a-lamp/>

在家具上吠叫命令似乎有点奇怪，但随着语音控制的家庭自动化平台成为常态，你可能会花更多的时间与你的灯具交谈，而不是与你的孩子交谈。在一个这样的项目中，[Becky Stern]使用了一个 Alexa Dot 和一个 ESP8266 来响应语音命令。

该设计使用 Alexa Dot 来解释语音命令，如“Alexa 开灯”。带有继电器羽翼的 ESP8266 用于打开和关闭实际的灯。两者之间的粘合剂是 [fauxmoESP](https://bitbucket.org/xoseperez/fauxmoesp) 库，它允许 [ESP8266 从 Alexa API](https://learn.adafruit.com/easy-alexa-or-echo-control-of-your-esp8266-huzzah) 接收命令。

这个项目最好的部分是灯本身，它有一个木制底座，非常适合这样的实验。[Becky Stern]在切割出足够的空间并用电子设备填充它方面做得非常好。额外的打磨和木材染色使该项目更加令人印象深刻，值得在客厅使用。这个想法可以很容易地扩展到其他自己的家居用品。查看下面的项目视频，想获得更多灵感，请看一看[忒伊亚物联网电灯开关](http://hackaday.com/2016/09/24/hackaday-prize-entry-theia-iot-light-switch/)。

 [https://www.youtube.com/embed/m5KUtmz_EYc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/m5KUtmz_EYc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

