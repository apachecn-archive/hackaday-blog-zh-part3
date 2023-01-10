# 美丽的人行道涂鸦机

> 原文：<https://hackaday.com/2015/12/11/beautiful-sidewalk-graffiti-machine/>

我们的英雄[Alex] [刚刚建造了一个人行道涂鸦机器](http://tinkerlog.com/2015/11/17/paint-machine/)，它看起来很美，所以请确保您查看休息下方的视频。但是不要忽视[Alex]的博客，以及贯穿始终的构建视频。([做轮子视频里的 t 恤很好看，顺便说一句](https://www.youtube.com/watch?v=IUsrZSteL60&t=2m44s)。)

这台机器本身基本上是一台两米宽的打印机，滚筒被驱动轮取代。框架由胶合板制成，外观精美，有助于减轻机器重量。一切都是用 DC 电机和同步带完成的，这意味着电机编码器和固件中的闭环控制。它通过一个用 ESP8266 制成的 WiFi 串行桥连接到[Alex]的手机。

从计划到软件，一切都可以在[【Alex】的 GitHub 上为项目](https://github.com/tinkerlog/PaintMachine/)获得。

 [https://www.youtube.com/embed/rzgcf4_C7zQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/rzgcf4_C7zQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



观看视频时，我们想到这台打印机不必局限于打印像 chalk jet 或 txt bomber 这样的光栅，而是可以打印实际的矢量图形——平滑曲线等等。让 2D 运动计划工作起来将会很棘手，而且它必须调整到喷雾罐的粉笔流，但是能够模仿一个真正的喷漆工的流体线将是值得的。如果我们幸运的话，更平滑的运动也将有助于理清 PID 控制的怪癖。