# 软件定义的无线电应用商店

> 原文：<https://hackaday.com/2016/05/07/software-defined-radio-app-store/>

理论上，软件定义无线电(SDR)几乎可以做任何你需要无线电做的事情。声音？数据？跳频？中继？没问题，你只要写出正确的软件，你就成功了。

这就是问题所在。你需要知道如何编写软件。 [LimeSDR](https://www.crowdsupply.com/lime-micro/limesdr) 是一个[开源 SDR](https://github.com/myriadrf/LimeSDR-USB) 与众筹运动。就其本身而言，这没什么特别的。有大量的 SDR 设备可用。LimeSDR 的有趣之处在于它使用 Snappy Ubuntu Core 作为一种应用商店。开发人员可以提供代码，最终用户可以轻松下载并安装这些代码。

当然，真正的价值在于人们是否真的用有意义的应用程序填满了商店。这当然适用于智能手机。如果必须自己写代码，有多少人会需要智能手机？一些用户甚至无法找到散布在互联网上的软件并安装它们。

另一方面，我们不禁认为，对于收音机来说，仅仅是应用程序只能让你到此为止。您真正需要的是可以轻松集成的组件。这是 GNU Radio 背后的想法([我们在](http://hackaday.com/2015/11/11/getting-started-with-gnu-radio/)之前已经介绍过 GNU Radio)。当然，LimeSDR 也支持 GNU Radio。然而，一个可以捆绑 GNU Radio 应用程序并允许轻松安装模块的应用程序商店将会广泛适用和有用。

另一方面，也许使用 GNU Radio 的人自己下载东西不会有问题。这就引出了一个问题:有多少消费者需要一种允许他们下载许多应用程序的 SDR？时间会证明一切。

你可以在下面看到一个关于 LimeSDR 的视频。在过去的几年里，我们已经谈论了很多关于 SDR 的话题，特别是 RTL-SDR 加密狗。不过，与 RTL-SDR 加密狗相比，LimeSDR 在价格和性能上是一大进步。

[https://player.vimeo.com/video/164304932](https://player.vimeo.com/video/164304932)