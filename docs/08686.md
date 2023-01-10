# K40 激光切割机，遇见树莓派

> 原文：<https://hackaday.com/2018/03/04/k40-laser-cutter-meet-raspberry-pi/>

廉价的中国 K40 激光切割机已经成为我们社区内许多小作坊的主食，以不太高的价格提供了一种不太大、不太强大的切割机。出厂时，这是一台并非没有缺陷的机器，有一整个社区的人都贡献了修复和升级，使这些刀具成为更有用的东西。

[Alex Eames]买了一台 K40，因为他是 Raspberry Pi 业务背后的人，当他从提供的基于 Corel 的软件切换到流行的开源 K40 Whisperer 时，他明显的选择是[在 Raspberry Pi](http://raspi.tv/2018/run-a-k40-laser-cutter-from-your-raspberry-pi-with-k40-whisperer)上运行它。由于 K40 Whisperer 是用 Python 写的，他推断 Pi 的 ARM 平台不会阻止它的使用，所以他开始工作并记录了过程和工作流程。

这是一个足够简单的过程，他的 K40 现在有一个 Pi，他可以将他的文件 SFTP 到其中，而不是大多数 K40 不可避免的旧笔记本电脑。社区创造了这么多 K40 改进，我们发现令人惊讶的是，一些有进取心的中国制造商没有看到赚一两个额外快钱的机会，并在工厂将其中一些集成到他们的产品中，包括许多单板计算机中的一个可以执行这项任务。

这些年来，我们已经报道了很多 K40 的故事，如果你是这台机器的新手，你可能想看一看[这个把它变成现实的故事](https://hackaday.com/2017/08/16/bringing-a-50-watt-laser-cutter-to-life/)。