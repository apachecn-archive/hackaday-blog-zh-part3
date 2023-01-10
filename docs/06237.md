# Pi 的 Btrfs

> 原文：<https://hackaday.com/2017/06/18/btrfs-for-the-pi/>

文件系统是典型的最终用户不太考虑的事情之一。显然，[seaQueue]不是一个典型的最终用户。他发布了一些关于如何在 Raspberry Pi 上运行备用文件系统 btrfs [的说明。](https://hackmd.io/IwFgZmBG0AwLQHYAcSxxAYwJzDlghgEwBscYGAJiZAlmDPUA)

对于任何处理存储的系统来说，正确的文件系统在性能和可维护性方面都有很大的不同。Linux，包括 Raspberry Pi 的大多数操作系统，使用 EXT 文件系统之一。这些都是身经百战，很好理解的。但是，还有其他文件系统，其中许多文件系统的高级特性优于某些应用程序的默认文件系统。

Btrfs，通常读作“黄油效率”，始于甲骨文，诞生于 IBM 的一篇论文中。它提供了[高级功能](https://en.wikipedia.org/wiki/Btrfs)，如池化、快照，以及将多个设备融合到一个逻辑设备中的能力。文件系统提供的一个显著特性是写入时复制。这意味着文件副本可以共享公共块，只要它们保持公共。压缩是可用的，就像用只读存储播种文件系统一样，这在一些嵌入式系统中非常有用。您也可以只使用 btrfs 来配置几种类型的 RAID。你可以在下面看到一个关于 btrfs 特性的视频演示。

[seaQueue]的帖子建议使用 8 GB 的 SD 卡，尽管你显然只能勉强挤进 4 GB 的 sd 卡。他还指出，btrfs 不支持交换文件(但您可以创建一个专用的交换分区)，某些工作负载可能会导致大量写入，这可能对 SD 卡和其他固态存储不利。他建议你可以使用固态硬盘，而不是 SD 卡或 USB 驱动器，这显然提供了更好的磨损均衡。

树莓派需要这种力量吗？也许不是。但是它仍然是一个很好的工具。我们可以想象，如果系统能够跨越多个卷，为备份创建快照，并实施 RAID，将会派上用场。

如果你想黑掉你自己的文件系统，那也是可能的。一个完整的文件系统是一个大工程，但是使用 [FUSE](https://hackaday.com/2013/11/06/writing-a-fuse-filesystem-in-python/) 你可以创建简单的文件系统，比如为 ssh 连接或压缩的归档文件做准备。最初的 Unix 哲学是一切都应该是一个文件。现代开发者在某种程度上已经远离了这一点，但是你仍然可以看到[偶尔的例子](https://hackaday.com/2012/11/29/phatio-uses-file-system-to-control-external-hardware/)。

 [https://www.youtube.com/embed/6DplcPrQjvA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/6DplcPrQjvA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

