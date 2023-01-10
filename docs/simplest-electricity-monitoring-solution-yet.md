# 迄今为止最简单的电力监控解决方案

> 原文：<https://hackaday.com/2015/09/12/simplest-electricity-monitoring-solution-yet/>

监控你家的能源使用是控制你的水电费的最好方法。毕竟，你不能管理你不能衡量的东西！唯一的问题是，大多数家庭能源监控系统都很笨重、复杂或昂贵。至少，直到现在。[Kevin]发明了一种新的基于粒子光子的电表,可以缓解所有这些问题。

粒子光子(我们对命名方案感到困惑，但相信这是过去被称为火花核心的新版本)是一个支持 WiFi 的开发板。[Kevin]使用两个，一个驱动显示器，一个监控用电量。这部分非常简单，每瓦特小时都伴随着电表上的 LED 脉冲，由 TLS257 光电压传感器检测。显示器是 Nextion TFT HMI(触摸屏),非常适合这种应用。数据由 OpenEnergyMonitor 平台的一部分 [emoncms](http://emoncms.org/) 收集，它将所有东西联系在一起。

对于一个已经做了[多次](http://hackaday.com/2011/05/13/monitor-your-homes-power-usage-on-the-cheap/)一次的项目来说，这个项目在保持美观的同时降低了价格。请务必查看下面的视频，看看它的实际效果。

 [https://www.youtube.com/embed/t3y08wBBB8c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/t3y08wBBB8c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

