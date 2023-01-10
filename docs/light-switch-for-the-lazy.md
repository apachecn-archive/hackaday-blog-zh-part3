# 懒人的电灯开关

> 原文：<https://hackaday.com/2017/12/10/light-switch-for-the-lazy/>

[威尔·唐纳森]为那些想涉足家庭自动化或者讨厌在上床睡觉前关掉卧室灯的人准备了一个快速的窍门:一个[遥控灯开关](http://www.instructables.com/id/Remote-Control-Bluetooth-Light-Switch/)！

这个远程开关使用一个 sg90 伺服系统、一个 Arduino Uno 和几对装配在原型板上的带有 HC-05 蓝牙模块的 ATtiny85s。3D 印刷安装架可以轻松安装在标准灯开关盖的顶部，同时仍然允许以传统方式翻转开关。这也是一个完美的临时解决方案——[唐纳森]目前正在租用他的公寓——或者对于那些不愿意弄乱他们住所电源的人来说。

 [https://www.youtube.com/embed/QmDzJaZzIgI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/QmDzJaZzIgI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



忠于这个项目的精神，[Donaldson]提供了关于如何设置和编程蓝牙模块和 ATtiny85 的教程链接，而不是长篇大论的解释。他确实向 ATtiny85 推荐了 SoftwareServo 库，因为标准的 Arduino 库不能在该芯片上工作，同时还提供了一个提示来确保它正确工作。

与 Google Home、 [Amazon Alexa](https://hackaday.com/2017/09/03/have-alexa-open-your-garage-door/) 和其他[家庭自动化](https://hackaday.com/2017/01/13/raspberry-pi-home-automation-for-the-holidays/)系统相比，这给了你一些入门级的功能，而成本只是它们的一小部分。