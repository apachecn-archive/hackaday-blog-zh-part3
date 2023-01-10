# 树莓派不怕幽灵，也不会融化

> 原文：<https://hackaday.com/2018/01/09/raspberry-pi-aint-afraid-of-no-spectre-and-will-not-meltdown/>

虽然人们普遍认为灾难和幽灵袭击从根本上来说确实是坏消息，但对其在现实世界中的直接实际影响却存在分歧。尽管保证在野外没有检测到攻击，并且有时间推出全面的缓解措施，但一些人希望现在就找到保护措施。如果你对一款没有崩溃或幽灵威胁的可用且易于安装的现代台式机感兴趣，[树莓派可以提供你所寻求的免疫力](https://www.raspberrypi.org/blog/why-raspberry-pi-isnt-vulnerable-to-spectre-or-meltdown/)。

[Eben Upton]使用 Python 的片段来解释旁路攻击，这是一个独立于 Raspberry Pi 的启发性阅读。当这些 ARM 内核执行推测指令*获取*时，它们不会推测*执行*或修改缓存。在目前的情况下，这让世界变得完全不同。

一个聪明的安全研究人员可能会在未来找到一种方法来利用投机取巧，声称 Raspberry Pi 具有更好的安全性是言过其实的。这个平台有自己的安全问题，但今天 Meltdown/Spectre 不在其中。这可能足以改变一些决定。

如果你需要留在 x86 的世界里，看看如何回到英特尔 486 的时代。

感谢[D00med]在评论中分享了我们的综述文章的链接。