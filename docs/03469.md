# 树莓 Pi 广播流媒体服务 Guts 雅马哈货架系统

> 原文：<https://hackaday.com/2016/09/09/raspberry-pi-radio-streaming-guts-yamaha-shelf-system/>

有几十个——几十个！—满足您当前音乐和流媒体需求的选项。寻找自己的东西，保留 90 年代的专用立体声系统，但具有现代无线集成，[thk4711]将旧的雅马哈 hifi 变成了 [Raspberry Pi 流媒体客户端](https://github.com/thk4711/raspiradio/wiki)。

就本案而言，一些修改允许[thk4711]使用所有现有的按钮，背板和屏幕的快速交换给他一个比他自己可以制造的更好的外壳。电源被证明是项目中最困难的部分，部分原因是当数字和模拟元件连接到公共地时，它们之间存在一些“数字噪声”干扰。这是通过实施两个变压器、一个 LM2596 稳压器和一个 LT1084 低噪声电源来解决的。

以 Raspberry Pi 2 为中心的设备支持网络电台、Spotify connect、Airplay、USB 和辅助输入。

 [https://www.youtube.com/embed/7hVFVi_NzME?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/7hVFVi_NzME?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



立体声由老式的数字按钮控制，或者通过苹果遥控器控制。该项目已经在 GitHub 上有完整的文档记录。如果你正在寻找你最喜欢的音乐的另一条线，咬一口这台收音机，它的[将音乐直接注入你的大脑](http://hackaday.com/2016/08/17/bone-conduction-skull-radio/)。