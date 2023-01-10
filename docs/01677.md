# 射频黑客:如何绕过滚动码

> 原文：<https://hackaday.com/2016/03/06/rf-hacking-how-to-bypass-rolling-codes/>

从现代遥控门锁发射器发射并由相关车辆接收的射频信号只使用一次。如果车辆再次看到相同的代码，它会拒绝该命令，但是在这些精心选择的单词中有一个漏洞。该代码必须由车辆计算机接收，然后才能添加到失效代码列表中。[AndrewMohawk]在他的博客中详细讲述了拦截钥匙链发射器发送的代码并阻止车辆接收该代码的过程[。休息后，你可以在他的录音室质量重现视频中看到这种攻击。](http://andrewmohawk.com/2016/02/05/bypassing-rolling-code-systems/)

[Andrew]使用[码棍一号](https://greatscottgadgets.com/yardstickone/) (YS1)，这是一种由计算机控制的亚 GHz 无线工具。YS1 使用 RfCat 固件，这是一个交互式 python shell，充当无线收发器的控制器。

这个系统并不是没有问题:不同的频率通常用于不同的命令，[Andrew]的脚本被设计成与开关键控(OOK)一起工作，这使得它在攻击使用频移键控(FSK)的系统时毫无用处。还有一个问题是使目标钥匙链失去功能，但你必须到[Andrew]的博客上阅读更多关于这方面的内容。

[https://player.vimeo.com/video/140315524](https://player.vimeo.com/video/140315524)

我们报道了以前的 SDR 黑客攻击，其目的是偷车和按门铃。你可能还会认出缩略图中的硬件设置是[Samy Kamkar]的 RollJam rig，你猜对了，这是另一篇关于[Samy]的项目之一的文章的强行插入的后续。