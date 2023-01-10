# 白帽僵尸网络感染，然后保护物联网设备

> 原文：<https://hackaday.com/2017/04/24/white-hat-botnet-infects-then-secures-iot-devices/>

[赛门铁克]报告称，Hajime 似乎是一种通过 telnet 传播的[白帽蠕虫](https://www.symantec.com/connect/blogs/hajime-worm-battles-mirai-control-internet-things)，目的是保护物联网设备，而不是实际做任何恶意的事情。

[Brian Benchoff]写了一篇关于[Hajime 蠕虫](http://hackaday.com/2016/10/20/hajime-yet-another-iot-botnet/)的很棒的文章，就在去年 10 月第一次发现这个故事的时候。当时，它看起来像是一个恶意物联网僵尸网络的开端，引发了一些 DDoS 问题。事情发生了疯狂的转变，现在看来，该蠕虫实际上正在保护受到另一个主要物联网僵尸网络(称为 Mirai 未来组合)影响的设备，该网络一直在发起 DDoS 攻击。最近一个[新 Mirai 未来组合变种](https://www.theregister.co.uk/2017/03/29/mirai_variant/)已经发起应用层攻击，因为它的源代码被上传到 [GitHub 账户](https://github.com/jgamblin/Mirai-Source-Code)并被改编。

Hajime 是一个比 Mirai 未来组合更复杂的僵尸网络，因为它是通过受感染设备点对点传播命令来控制的，而后者使用硬编码地址来命令和控制僵尸网络。Hajime 还可以更好地隐藏自己，设法隐藏自己不运行进程，并从设备中隐藏其文件。

> 作者可以随时向网络中任何受感染的机器打开一个 shell 脚本，代码是模块化的，因此可以随时添加新的功能。从代码中可以明显看出，设计这个蠕虫花费了大量的开发时间。

那么这一切将走向何方？到目前为止，这开始看起来像一场正义与邪恶的网络战争。或者这是网络黑手党之间的地盘之争。只有时间能证明一切。