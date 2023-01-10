# 用一个完全机械的老式遥控器指挥 Alexa

> 原文：<https://hackaday.com/2017/04/02/command-alexa-with-a-completely-mechanical-vintage-remote-control/>

任何有祖父母的人都知道，在过去，电视没有遥控器。你的父母可能还在抱怨，当他们还是孩子的时候，为了在三个可用的频道之间切换，他们被迫走到电视机前。在这个科技奇迹的现代，我们有语音控制、可编程触摸屏遥控器和流媒体服务，可以自动播放你正在疯狂观看的整季节目。然而，在此之前，在无处不在的红外遥控器出现之前，电视制造商正在尝试各种方法，让孩子们不必每次需要换频道时都跑到客厅里。

早期的远程控制只是简单的有线事务——没什么好奇怪的。但是，没过多久，无线控制的方法就被引入了。早期的一项努力叫做闪光灯，它将光线照射到电视机的光电管上来控制它。当然，它也可能被意想不到的光源控制，用户必须有良好的目标来击中传感器。这些问题很快导致了天顶空间命令遥控器的引入，它使用超声波频率来控制电视。

天顶空间指挥部特别有趣的是，它完全是机械的，不包含任何电子设备。不需要更换电池，因为它使用超声波，所以不需要直接对着电视机。设计太空指挥部的 Zenith 工程师罗伯特·阿德勒通过使用物理按钮来实现这一点，这些按钮触发弹簧加载的锤子来击打调谐到必要频率的金属杆。这就产生了一种独特的咔哒声(因此有了“咔哒声”这个术语)，发出适当的超声波频率，电视机中的电路就会做出反应，改变频道。

在下面的视频中，【蒙他·埃尔金斯】[分解了一个老式的天顶空间指令](https://www.youtube.com/watch?v=JrhKW20DIvA&feature=youtu.be)向我们展示内部机制是如何工作的。然后，他进一步演示了他是如何构建一个系统来响应遥控器的。使用一个 Teensy，一个 Arduino Uno 和一点语音合成，系统被 Space 命令触发，然后说出一个命令，然后由 Amazon Alexa 注册。

想了解更多关于全能遥控器的信息吗？那么你首先要回答这个问题:[遥控器有多旧了？](http://hackaday.com/2017/03/16/retrotechtacular-how-old-is-the-remote/)

 [https://www.youtube.com/embed/JrhKW20DIvA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/JrhKW20DIvA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

