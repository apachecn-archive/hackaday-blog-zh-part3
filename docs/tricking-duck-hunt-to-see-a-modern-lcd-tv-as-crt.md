# 诱骗猎鸭者将现代液晶电视视为 CRT

> 原文：<https://hackaday.com/2016/08/30/tricking-duck-hunt-to-see-a-modern-lcd-tv-as-crt/>

20 世纪 80 年代和 90 年代，游戏机的必备外设是光枪。镜头和光电池安装在一个枪状的塑料外壳中，控制台可以计算出当它的触发器被按下时，它在屏幕上指向哪里，方法是使屏幕闪烁白光，并感应屏幕上的飞行点触发光电池的时间。

不幸的是，光枪游戏来自 CRT 电视的时代，它们不能与现代的 LCD 一起工作，正如我的同事[Will sweat man][去年年底雄辩地说明的](http://hackaday.com/2015/11/16/resurrecting-duckhunt/)。阴极射线管在屏幕上显示圆点，与控制台输出完全同步，而液晶显示器捕捉一整帧，处理并一次显示出来。所有的计时都丢失了，并且控制台不再能够感知位置。

[Charlie]用一些最新的技术和一点横向思维解决了这个问题，[成功地让轻型枪械游戏起死回生](https://www.youtube.com/watch?v=DzIPGpKo3Ag)。他使用 Wiimote 通过树莓 Pi 在电视顶部感应杆感应枪指向何处，并将位置信息输入 Arduino。然后，他从控制台获取视频信号，并去除同步脉冲，这些脉冲也会传送到 Arduino。知道了位置和时间，Arduino 就可以在 CRT 部分被点亮的精确时刻闪烁粘在光枪枪管末端的白色 LED，就游戏而言，它已经收到了它所期望的输入。

他在休息时间下方的视频中解释了计时问题及其解决方案。然后，他向我们展示了那个时代使用该设备的各种游戏机上的游戏。更多信息和他的代码可以在他的 [GitHub 库](https://github.com/charcole/LCDZapper)上找到。

 [https://www.youtube.com/embed/DzIPGpKo3Ag?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/DzIPGpKo3Ag?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



我们之前已经介绍过[查理]在复古游戏领域的工作，他的[HDMI mod 用于近地轨道 MVS](http://hackaday.com/2015/02/13/hdmi-audio-and-video-for-neo-geo-mvs/)。控制台光枪已经在这些页面上出现了很多次，最近的一次是[这个视频合成器](http://hackaday.com/2016/02/25/nes-light-gun-turned-video-synthesizer/)，但它是[这个燃烧的激光模块](http://hackaday.com/2012/09/21/nes-light-gun-gets-a-burning-laser-upgrade/)，大多数 20 世纪 80 年代的孩子会放弃任何东西来拥有它。