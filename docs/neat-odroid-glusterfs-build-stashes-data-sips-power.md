# 整洁的 Odroid 和 GlusterFS 构建存储数据，吸取能量

> 原文：<https://hackaday.com/2018/06/14/neat-odroid-glusterfs-build-stashes-data-sips-power/>

我们大多数人都会积累东西，比如装满旧电缆的抽屉和装满数据的硬盘。Reddit 用户[BaxterPad]并不担心这些事情，因为他建立了一个令人印象深刻的[网络连接存储(NAS)系统，可以容纳超过 200TB 的数据](https://www.reddit.com/r/DataHoarder/comments/8ocjxz/200tb_glusterfs_odroid_hc2_build/)。这足以令人印象深刻，但真正的艺术性在于他是如何做到这一点的。他使用运行 GlusterFS 的 [ODroid HC2](https://odroidinc.com/collections/odroid-single-board-computers/products/odroid-hc2-home-cloud-two?variant=3423240355866) 单板计算机构建了这个系统，结合了巨大的冗余和低功耗。

Odroid HC2 是一台小巧的单板计算机，提供单一 SATA 接口，运行 Linux。[BaxterPad]购买了 16 台这样的设备，并在每台设备上安装了相当大的硬盘。然后，他安装了 [GlusterFS](https://www.gluster.org/) ，这是一个分布式网络文件系统，可以自动将数据分散到这些驱动器上，确保每一位数据都存储在多个位置。不过，它将这些数据以单个驱动器的形式呈现给用户，因此用户不必担心特定的数据存储在哪里。如果任何驱动器或 HC2 系统出现故障，NAS 系统将继续工作，不会出现任何问题。

像这样的系统并不新鲜:像 [FreeNAS](http://www.freenas.org/) 和 [UnRAID](https://lime-technology.com/) 这样的软件可以让你轻松地构建一台计算机，将数据分布在多个驱动器上，如果其中一个出现故障，它还可以继续运行。这里的不同之处在于，该系统易于扩展，并且可以在一台或多台计算机出现故障时存活。如果运行 FreeNAS 服务器的电脑死机，您的数据将无法访问，直到它恢复运行。如果这个系统中的一台或多台 Odroid HC2 计算机死亡，它将继续运行。它也更容易扩展:只需购买另一个 HC2，插入硬盘并运行几个命令，它就会无缝地添加到可用存储中。

[BaxterPad]还指出，该系统并不消耗太多电力:每个 HC2 消耗大约 12 瓦，整个系统(包括运行 VMware 的机架式 PC)消耗不到 250 瓦。这比典型的高端服务器系统少得多。