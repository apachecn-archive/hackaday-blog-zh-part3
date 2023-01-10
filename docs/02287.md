# AV 远程控制团队 Arduino 与–Visual Basic？

> 原文：<https://hackaday.com/2016/05/15/av-remote-control-teams-arduino-with-visual-basic/>

一个庞大的安装基地的电动扬声器来自一个已倒闭的制造商，以及越来越少的可用遥控器。听起来像是 AV 专业人员的噩梦——除非你亲自动手，用 Arduino 和定制软件取代 IR 遥控器。

从声音来看，[史蒂夫]的团队正在为一个公司会议室开发 AV 设备——有源扬声器和液晶投影仪。给他们带来麻烦的是扬声器，或者说是容易损坏或丢失的遥控器。在最后一个人死去之前，[史蒂夫]用 Arduino 和非远程库捕获了每个按钮的红外代码。有了代码，让 Nano 用红外 LED 发送代码就变得非常简单了。但这个项目的独特之处在于，控制 Arduino 的自定义 GUI 是用人人都讨厌的语言 Visual Basic 编写的。这是一个肮脏的小秘密，许多公司仍然依赖于 VB，这是一个很好的变化，看到对备受指责的语言的一点点爱。而且它完成了任务。

想深入了解 IR 吗？也许这本关于用 Arduino 克隆红外遥控器的入门书会有所帮助。另一个 VB 大放异彩的项目，看看[这个声控 RGB LED 灯](http://hackaday.com/2014/08/17/voice-controlled-rgb-led-lamp/)。