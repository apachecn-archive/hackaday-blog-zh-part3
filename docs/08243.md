# 掌握熔毁更新的影响，敬请关注 Spectre

> 原文：<https://hackaday.com/2018/01/09/getting-a-handle-on-meltdown-update-impact-stay-tuned-for-spectre/>

当在最初的披露计划之前，关于 Meltdown 和 Spectre 的新闻爆出时，消息像野火一样传播开来，很难区分事实和猜测。一个普遍重复的说法是，该修复将使计算机在某些工作负载下的速度降低 30%。微软今天发布的一份报告称，使用 2015 年后硬件的“普通用户”不会注意到这种差异。虽然没有具体数字，但他们提到，他们预计运行 2015 年之前的硬件的人在应用补丁后会体验到明显的速度变慢。

Meltdown 更新的影响更容易归类:它们减缓了从用户的应用程序级代码到系统级内核代码的转变。好消息是:在 Meltdown 出现之前，这种转变已经是一种令人扫兴的表现了。有大量的工具(设计模式、库和 API)可以帮助软件开发人员减少用户内核转换的次数。

已经被编写来最小化内核转换的性能敏感代码将很少受到崩溃更新的影响。这包括大多数游戏和主流应用。这些更新将对那些经常在内核和用户世界之间切换的少数应用程序产生更大的影响。反病毒软件([有自己的问题](https://support.microsoft.com/en-us/help/4072699/january-3-2018-windows-security-updates-and-antivirus-software))有理由这样做，并可能最终导致普通用户看到的大多数速度变慢。

即使通过微软的玫瑰色眼镜来看，服务器及其大量的磁盘和网络 IO——以及内核使用——将会有一段糟糕得多的时间。以至于微软建议管理员“为您的环境权衡安全性和性能”。

Spectre 更新的影响很难确定。推测性执行和缓存在现代 CPU 中太重要了，不能“随便”关掉。修复将会更加复杂，我们必须等待他们推出([颠簸和所有](https://support.microsoft.com/en-us/help/4073707/windows-os-security-update-block-for-some-amd-based-devices))之前，我们有一个更好的画面。

正如一些科技巨头[目前所说的](https://security.googleblog.com/2018/01/more-details-about-mitigations-for-cpu_4.html)，这种影响可能最终可以忽略不计，这可能符合你的体验，除非你正在运行一个服务器场。但是即使他们错了，你仍然会比[英特尔 486](https://hackaday.com/2018/01/07/go-retro-to-build-a-spectre-and-meltdown-proof-x86-desktop/) 或[树莓 Pi](https://hackaday.com/2018/01/09/raspberry-pi-aint-afraid-of-no-spectre-and-will-not-meltdown/) 快得多。

你们谁有号码了吗？

[via [The Verge](https://www.theverge.com/2018/1/9/16868290/microsoft-meltdown-spectre-firmware-updates-pc-slowdown)