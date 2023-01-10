# 树莓派开启了

> 原文：<https://hackaday.com/2016/06/28/raspberry-pi-gets-turned-on/>

Raspberry Pi 和其他类似的基于 Linux 的单板计算机简化了许多项目。然而，Linux 的一个问题是它不喜欢被突然关闭。情况已经有所好转，您当然可以配置一些东西来最小化风险，但是——一般来说——在 Linux 系统运行时关闭它最终会导致文件系统损坏。

如果你的项目有一个接口，你总是可以提供一个关闭选项，但是如果你的应用程序是无头的，那就没用了。您可以提供一个关机按钮，但这留下了重新打开设备的问题。

[Ivan] [用 Arduino 解决了这个问题](http://www.ivancreations.com/2016/06/physical-onoff-button-for-raspberry-pi.html)(见下面的视频)。简单地说，Arduino 读取一个按钮，并使用一个 FET 来关闭 Pi 的电源。Arduino 的原因是微型处理器(它消耗的功率小于 Pi，并且不介意突然关闭)可以登录 Pi 并正确关闭它。不过，真正的优势在于，您可以使用其他 Arduino 输入来确定何时打开和关闭 Pi。

例如，很容易想象汽车应用中的 Pi，Arduino 会检测到点火开关关闭一段时间，然后继续关闭 Pi。或者可能需要在运动传感器触发时打开 Pi，然后在特定时间段内没有运动时再次关闭。用 Arduino 构建这些策略都很简单。

我们已经看到[一个类似的项目](https://hackaday.com/2015/07/18/arduino-and-ir-remote-turn-off-raspberry-pi/)，它使用一个红外遥控器作为触发器，而不是一个物理按钮。如果你担心 Pi 会意外断电，你可以考虑用一个[备用电池](https://hackaday.com/2013/11/17/battery-backup-for-raspi-keeps-your-data-safe/)。如果用常规电力给码头供电对你来说太难，那么[试试蒸汽](https://hackaday.com/2016/03/17/steam-powered-raspberry-pi-zero-doesnt-get-any-more-steampunk/)。

 [https://www.youtube.com/embed/jeAihve5bdw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/jeAihve5bdw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

