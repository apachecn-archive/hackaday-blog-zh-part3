# 通过电力电缆从空气隙网络中获取数据

> 原文：<https://hackaday.com/2017/08/01/getting-data-out-of-air-gapped-networks-through-the-power-cable/>

如果你是一个保管敏感信息或基础设施的组织，你直接把它放在公共互联网上是鲁莽的。无论你的安全措施有多好，总会有歹徒绕过它，进行各种恶作剧的风险。因此，采用的解决方案是将这些敏感设备与外界物理隔离，形成一个空气间隙。没有东西可以进来，也没有东西可以出去，理论上也是如此。

嗯，反正就是这个*理论*。[Davidl]给我们一些工作，[在一些空气间隙网络](https://pushstack.wordpress.com/2017/07/24/data-exfiltration-from-air-gapped-systems-using-power-line-communication/)上打了一个洞，允许低速数据逃离空气间隙，即使它不允许反向。

那么这个看似不可能的任务是如何执行的呢？答案来自电源电气基础设施，如果空气间隙由电源电缆桥接，则电源电缆上的负载可以通过改变连接到它的计算机所承担的工作来调制。这种调制可以用电流互感器来检测，甚至可以通过在气隙外放置一个 UPS 或电表来检测。

当然，黑客时代的读者都是正直守法的好公民，对他们来说，这些事情纯粹是学术兴趣。尽管如此，这篇文章还是非常详细地探讨了这个问题，读起来很有意思。

我们之前已经通过各种技术触及过这个主题，如[广播无线电干扰](http://hackaday.com/2016/07/05/data-exfiltration-with-broadcast-radio-and-cd-rom-drives/)和来自风扇的[噪音](http://hackaday.com/2016/07/01/bridging-the-air-gap-data-transfer-via-fan-noise/)，以及[深度特写](http://hackaday.com/2017/02/02/hacking-the-aether/)。