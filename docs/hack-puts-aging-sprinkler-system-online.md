# 黑客将老化的洒水系统放到网上

> 原文：<https://hackaday.com/2015/09/09/hack-puts-aging-sprinkler-system-online/>

节约用水是很多人的想法，使用旧的洒水系统，人们可能无法最好地控制何时何地给草坪浇水。面对这样一个系统，[费利克斯]决定侵入他的系统，[增加更好的计算机化日程安排和互联网远程控制](http://lowpowerlab.com/blog/2015/08/31/sprinkler-controller-automation/)。

操作的大脑由一个 [Moteino](http://lowpowerlab.com/moteino) 处理，这是一个 Arduino 兼容的微控制器板，板上有 WiFi。为了与喷水灭火系统接口，制作了一个接口 PCB。该接口有一个板载降压电源，用于将微处理器和 74HC595 移位寄存器的洒水器的 24 伏交流电源调节到 5 伏 DC。

移位寄存器的输出连接到一个管脚头，通常股票计算机会插在那里。通过一个小软件和一个手机应用程序，新的微控制器只需用拇指一推，就可以接管洒水器三端双向可控硅开关的开关区域。

休息之后，请加入我们，观看一段快速演示视频。

 [https://www.youtube.com/embed/WWMZoeMzi2s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/WWMZoeMzi2s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

