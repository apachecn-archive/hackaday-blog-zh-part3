# 世界上最愚蠢的固态硬盘黑客

> 原文：<https://hackaday.com/2018/02/12/worlds-stupidest-solid-state-disk-drive-hack/>

这个标题可能看起来有点刺耳，但它是从[Linus Tech Tips] 的视频中直接引用的[，你可以在下面看到。他拿起一块板，这是一个 RAID 0 控制器，可用于多达 10 个 SD 卡，所以你可以将它们用作传统的 SATA SSD。当然，该频道的口号是“对不可能的问题不切实际的解决方案”，但即使是他自己也承认，这是非常不切实际的。](https://www.youtube.com/watch?v=3frnBoqqI_Q)

对我们来说，嘲笑任何类型的黑客行为都是很奇怪的，但老实说，很难看出这有什么价值，除了认为一些工厂生产这些主板希望获利是很有趣的。不过，除了有趣之外，这也是设计行业的一个很好的练习。例如，当你设计一辆汽车时，你希望它是安全的，但由于成本、重量和燃料消耗，你不能用四英寸厚的钢制造车身。所以你通过权衡来平衡这些顾虑。

这里的交易大多是单边的。我们认为 SD 卡很便宜，尽管现在一个合适的固态硬盘的价格也没那么高。SD 卡相对较慢，RAID 0 控制器有助于解决这个问题——至少应该如此。当然，不利的一面是，如果 10 张卡中的任何一张卡出现故障，整个阵列都会出现故障，因为 RAID 0 没有冗余。此外，尽管顺序数据的性能足够好，但[Linus]测量了随机数据的性能，结果很糟糕。我们不知道这是设计中固有的还是执行中的缺陷。

慷慨地说，假设你为每张 128 GB 的 SD 卡支付 40 美元，那就是 400 美元。你可以很容易地以同样的价格买到 1TB 的固态硬盘。[Linus]不知道为什么要做这些板子，我们也不知道。也许有人会在评论里有想法。

现在，如果你黑掉主板，使其不使用 RAID 控制器，而只是将它用作十个 SD 卡的载体，那么对于数据记录器来说[就太棒了。也许如果你正在](https://hackaday.com/2016/11/04/add-data-to-your-shipping-suspicions-with-this-power-sipping-datalogger/)[打造一台定制的笔记本电脑](https://hackaday.com/2017/10/24/diy-laptop-aims-for-complete-hardware-freedom/)，并希望它有点像 Rube Goldbergesque，这可能是一个好的开始。

 [https://www.youtube.com/embed/3frnBoqqI_Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/3frnBoqqI_Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

