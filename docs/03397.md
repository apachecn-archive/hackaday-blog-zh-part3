# 树莓派蜂巢思维

> 原文：<https://hackaday.com/2016/08/29/raspberry-pi-hive-mind/>

设置计算机集群曾经是大型数据中心和实验室使用的高端技巧。毕竟，买一堆，比如说，VAX 电脑，很快就会烧钱(甚至不算运营费用)。然而今天，我们大多数人都有一大堆树莓派电脑。

因为 Pi 运行 Linux(或者至少可以运行 Linux)，所以有大量的工具可以做任何事情。诀窍是弄清楚如何安装它。集群几个 Linux 机器并不一定很困难，但是如果不使用特殊的工具，就需要做大量的工作。其中一个工具是 Docker，特别是 Docker 群体模式。[Alex Ellis]有一个很好的[视频](https://www.youtube.com/watch?v=0QtVQLjDhMI)(见下文)展示了一个 28 CPU 集群的细节。

使用 Docker 网站上的指令很容易建立一个蜂群。如果你不熟悉 Docker，它几乎(但不完全)是一个轻量级的虚拟机管理器。一个真正的虚拟机管理器伪装成一个硬件，这样 Linux(或另一个操作系统)就可以在其上启动并运行应用程序。Docker 是一个容器管理器，这意味着它不会伪装成一个硬件，它会伪装成一个正在运行的操作系统。程序看到自己的文件系统和其他资源，但实际上，只有一个内核在主机硬件上运行。

这个想法类似于在 chroot 监狱里运行一些东西。该程序可以对其文件系统进行更改，而不会扰乱系统的其余部分。Docker 还提供了其他种类的隔离。然而，真正吸引人的是它可以自动加载预定义环境的图像。这允许开发者提供本质上预装在他们自己的私有操作系统中的包。

这很重要，因为这意味着服务可以在集群中的任何节点上运行。这让您可以在多个节点之间平衡负载。您还可以进行滚动更新，并从群集中动态添加或删除计算机。

当然，我们已经在之前看到过[星团。就连小小的](https://hackaday.com/2016/05/26/raspberry-pi-cluster-build-shows-how-and-what/)[圆周率为零的](https://hackaday.com/2016/01/25/raspberry-pi-zero-cluster-packs-a-punch/)也能参与进来。如果你想了解更多关于 Docker 的知识，你可以随时阅读[官方文档](https://docs.docker.com/engine/understanding-docker/)。鉴于 Linux 在嵌入式系统中的流行，部署预配置的应用程序可能是一种有趣的方式。

 [https://www.youtube.com/embed/9m352pAoaow?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/9m352pAoaow?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

