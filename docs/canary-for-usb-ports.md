# USB 端口的金丝雀

> 原文：<https://hackaday.com/2017/04/04/canary-for-usb-ports/>

如果你是一个偏执的系统管理员，[errbufferoverfl]有一个软件可以跟踪任何时候有人将基于 USB 的设备从工作站上插入或断开。

[命名为 USB 金丝雀](https://github.com/probablynotablog/usb-canary)，【errbufferoverfl 的】工具是用 Python 写的。然而，即使 Python 是跨平台的，USB Canary 目前只在 Linux 上工作。但是，不用担心:[errbufferoverfl]已经在 Windows 和 Mac 版本上运行了。

首先，USB 金丝雀观察 USB 连接器的任何活动，并记录它看到的任何东西。此外，当 USB 设备被插入或拔出时，USB Canary 可以通过 Twilio API 提供的 SMS 消息提醒工作站的所有者，在 Slack 通道中发布消息，甚至发出声音来提醒附近的系统管理员。此外，USB 金丝雀可以配置为只在工作站锁定时运行(如果你不是完全偏执)。

【errbufferoverfl 的】USB 金丝雀诞生于对当前工作站监控工具的不满。你看，大多数工具只在有人登录后才通知用户*。[errbufferoverfl]指出，不登录也有自动化攻击的手段，我们可以想到很多注销后可以做的令人讨厌的事情。*

虽然 USB 金丝雀不会保护你免受 [-220V](http://hackaday.com/2015/10/10/the-usb-killer-version-2-0/) 的攻击，但它至少可以警告一个 [BadUSB 攻击](http://hackaday.com/2014/10/05/badusb-means-were-all-screwed/)。但是，对于真正的偏执狂来说，为什么不试试 [GoodUSB](http://hackaday.com/2017/03/02/good-usb-protecting-your-ports-with-two-microcontrollers/) ？

[通过[出血计算机](https://www.bleepingcomputer.com/news/software/usb-canary-sends-an-sms-when-someone-tinkers-with-your-usb-ports/)