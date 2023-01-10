# 如果你从过程中学到了什么，这是一个愚蠢的项目吗？

> 原文：<https://hackaday.com/2017/07/01/is-it-a-stupid-project-if-you-learn-something-from-the-process/>

坐立不安的纺纱工——现在太热了！

[Ben Parnas]和工程愚蠢的合作者[Greg Daneault]最近在马萨诸塞州剑桥举办的波士顿愚蠢黑客马拉松上带来了他们的物联网坐立不安旋转器…旋转器。一位杰出的芬兰人。是的，没错:旋转智能手机，旋转器也会跟着旋转。傻？也许吧，但有充分的理由。

一部分是对云技术的讽刺，一部分是学习经验，短短八个小时的修补让这个怪诞的、基于 ESP32 的设备变得栩栩如生。ESP 可以作为 Arduino 引导加载程序，但您会希望使用 ESP-IDF sdk，从而能够更广泛地使用芯片。

两人开发了一个从手机陀螺仪中提取数据的应用程序，设置 spinner-bot 访问 WiFi，并通过基于云的服务器“spincloud”从智能手机请求旋转数据包。这两款设备都可以作为客户端来规避现有的物联网服务。

[Parnas]规定——理论上——你可以用这个设置控制你能想象到的任意多的旋转器，但是一个对我们来说已经够傻的了。不管可笑与否——如果你学到了什么，那么很可能是值得的！所以，继续研究这些想法，你也许能向所有关注你的人证明这一点。

首先，你可以告诉他们你在一个好公司。

 [https://www.youtube.com/embed/kRJj4xgd7W4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/kRJj4xgd7W4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

