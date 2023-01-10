# 无线门铃黑进动手 MQTT 教程

> 原文：<https://hackaday.com/2017/03/02/wireless-doorbell-hacked-into-hands-on-mqtt-tutorial/>

这个项目本身非常简单:当无线门铃响起时，通过 MQTT 获得推送通知。但是正如[罗宾·赖特尔]指出的，作为“你好，世界！”对于不熟悉一门语言的程序员来说，编程是一个由来已久的传统，所以他的项目在很大程度上是同一传统的硬件体现。下面附带的视频构建日志是一个旋风之旅，它将让新手离开地面，踏上通往 MQTT 荣耀的道路。

[Robin]为这个初级读本选择的硬件非常简单——一个无线门铃，由一个电池供电的按钮和一个插入式接收器组成，当你有访客时，它会发出悦耳的嘟嘟声。[Robin]试图通过逆向工程拆卸接收器，但他明智地选择了阻力最小的路径，并决定监控按钮按下时闪烁的 led。一个 RFduino 是从[Robin]组织得非常好的零件箱中挑选出来的，并为这项工作连接起来。duino-fied 门铃通过蓝牙与 Raspberry Pi 上的 MQTT 经纪人进行对话，该经纪人还负责向他的手机发送推送通知。

然而，构建日志的核心是设置 MQTT 的细节。我们已经发布了很多关于 MQTT 的内容，包括关于这个主题的[【埃利奥特·威廉姆斯】](http://hackaday.com/2016/05/09/minimal-mqtt-building-a-broker/)。但是本教程非常具体，这种东西你可以跟着做，偶尔暂停一下视频，然后让一个工作系统快速启动并运行。这里有很多适合初学者的东西，即使是老手也会学到一两个技巧。

 [https://www.youtube.com/embed/J_BAXVSVPVI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/J_BAXVSVPVI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

