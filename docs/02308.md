# 设计高性能并行个人集群

> 原文：<https://hackaday.com/2016/05/09/designing-a-high-performance-parallel-personal-cluster/>

Kristina Kapanova 是保加利亚科学院的博士生。她的研究是模拟半导体设备中的量子效应，但这个研究领域需要一台超级计算机进行数十亿次计算。该学院有一台合适的超级计算机，并且正在添置一台新的，但有一段时间，克里斯蒂娜和她那些吃拉面的同事们没有一台大的计算设备。为了解决这个问题，克里斯蒂娜用现成的 ARM 板建造了自己的超级计算机。

 [https://www.youtube.com/embed/_IqSbW6drrw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/_IqSbW6drrw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



由于超级计算机的需求——即内存容量和纯粹的处理速度——树莓 Pis 和 BeagleBones 是不可能的。这台超级计算机只是需要更快的速度。这让 Kristina 在 Odroid X2 和 Radxa 摇滚之间做出选择。这两款单板计算机都有一个四核 ARM Cortex A9，2GB 内存，可以轻松地从 5V 电源供电。当时在保加利亚只有 Radxa Rock 可以买到，是唯一的选择。

在 Slashdot 上的 Beowulf 笑话出现之前，个人集群就已经存在了，但最近几年，像 Raspberry Pi 这样的廉价 ARM 板让集群计算重新焕发了生机。[有 64 节点集群](http://hackaday.com/2012/09/12/64-rasberry-pis-turned-into-a-supercomputer/)， [120 节点集群](http://hackaday.com/2014/10/07/120-node-rasperry-pi-cluster-for-website-testing/)，每台机器上都有显示器，还有一些是用乐高搭建的。Kristina 的集群与这些 Pi 集群没有太大的不同——她所需要的只是八块板、一个以太网交换机、一个大 USB 集线器、几根电缆和一个机箱。通过几个脚本来检测热插拔的主板，一切都正常工作，只需要花费大约€500。

构建一个集群并不是做一个漂亮的外壳和连接所有的电路板。最大的问题是让软件运行起来。为此，Kristina 删除了 Radxa 板上的 Android 安装，并用 Linaro 替换，并添加了一些额外的包，包括在集群中传递消息的 MPI、 [OpenMP](http://openmp.org/wp/) 和 Fortran。是的，Fortran。毕竟，这是科学计算。

集群完成后，是时候实际使用它了。虽然这个集群不是一台超级计算机，但它在处理计算要求高的问题时比单个快速桌面处理器要快得多。Kristina 正在使用这个集群进行自然语言处理、深度神经网络和量子物理模拟。利用这个集群，Kristina 能够运行泡利不相容原理的模拟，结果发表了一篇论文。对于€500 现成的电子产品和几个周末摆弄几块电路板来说，这已经不错了。