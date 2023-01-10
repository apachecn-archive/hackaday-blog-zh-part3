# 通过广播电台和光盘驱动器进行数据渗透

> 原文：<https://hackaday.com/2016/07/05/data-exfiltration-with-broadcast-radio-and-cd-rom-drives/>

在个人电脑上播放的第一首音乐并不是出自花哨的声卡，甚至也不是 DAC。个人电脑中的第一个音频系统仅仅是把一个 AM 收音机举到箱子上，疯狂地闪烁着地址针。这对于自制计算机非常有效，在自制计算机中，EMC 法规遵从性甚至不是事后才想到的，但这种技术今天仍然有效。[Chris] [在收音机上播放音乐](https://www.youtube.com/watch?v=xSj5skknXWg&feature=youtu.be)通过系统总线发送位，完全不使用任何电线。

[【克里斯】](https://github.com/anfractuosity/musicplayer)的代码是基于[【完全体面】](https://github.com/fulldecent/system-bus-radio)的早期作品，工作原理也差不多。要通过无线电播放声音，代码只需在波形应该为高电平时写入内存中的某个位置，而在波形为低电平时则不写入。

当然，通过空气间隙泄露信息的能力有一些更邪恶的目的，但是[克里斯]也有另一种方法可以做到这一点，这是一台被暴风雨屏蔽的计算机无法攻破的。他可以通过打开和关闭 CD-ROM 驱动器，用网络摄像头捕捉这些位，一次发送一位。有用吗？很难想象这种设置如何能够捕获任何有价值的数据，但这是一个概念证明。