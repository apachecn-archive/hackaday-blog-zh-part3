# 这个 VU 计是装在扬声器里的

> 原文：<https://hackaday.com/2015/11/29/this-vu-meter-is-built-into-the-speaker/>

根据你正在听的音乐，看着 VU 节拍随着音乐跳动总是一段美好的时光。那么，为什么不将 VU 测量仪集成到音频源中呢？这就是[Matikas]所做的，这非常奇妙。

他从一对扬声器开始，拿起一些 NeoPixel LED 灯条。小心地将 LED 条包裹在每个扬声器的内侧周围，LED 安装在扬声器格栅的后面，当它们打开时，给它一种凉爽的效果。

为了控制 LED，他使用 Arduino Uno (Atmega328p)来测量音频电平，以调制 LED 输出。稍后一点软件(如果你感兴趣，分享到 [GitHub](https://github.com/Matikas/VU_meter) 上！)和 VU 米准备行动——看看吧！

 [https://www.youtube.com/embed/HYQ-gCvjnwY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/HYQ-gCvjnwY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



至于 VU 米去，我们不能忘记这个可怕的[巨型水管 VU 疯狂展示](http://hackaday.com/2012/05/04/huge-water-and-light-vu-meter-plus-more/)。