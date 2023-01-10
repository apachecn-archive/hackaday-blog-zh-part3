# 头脑风暴叉车机器人会抢走你的工作

> 原文：<https://hackaday.com/2017/11/17/mindstorms-forkliftbots-gonna-take-your-job/>

随着机器人技术的每一次进步，我们越来越接近能够从亚马逊订购商品，并且没有人类参与送货。这个梦想的关键一步是:仓库机器人，能够控制和盘点的智能叉车，以及装满托盘的整个仓库，而不需要肉类社区的参与。[Thomas Risager]设计了这样一个系统，作为他软件工程硕士论文的一部分。它由五个协同工作的乐高 Mindstorms 机器人组成，通过 WiFi 连接到中央笔记本电脑。Mindstorms 的原生 OS 不支持 WiFi(！！！)所以他用 Java 开发的运行在 LeJOS 下的软件刷新了 EV3 的 ARM9 芯片。在笔记本电脑端,[Thomas]编写了一个 C++应用程序来处理叉车的协调和路线安排。我们可以看到许多疲惫的叉车司机准备休息一下，让机器人做全职工作。

这些机器人使用 WiFi 连接中央笔记本电脑。Mindstorms 的原生 OS 不支持 WiFi(！！！所以[Thomas]用 Java 开发的运行在 LeJOS 下的软件刷新了 EV3 的 ARM9 芯片。在笔记本电脑端，他编写了一个 C++应用程序来处理叉车的协调和路线安排。[Thomas]正在[分享他的叉车设计](https://www.youtube.com/watch?v=upQARrhp4DE)。

现在扩大规模——也许用我们之前发表的 [DIY 叉车](https://hackaday.com/2013/02/13/diy-forklift-for-the-home-shop/)?我们可以看到许多疲惫的叉车司机准备休息一下，让机器人做全职工作。

 [https://www.youtube.com/embed/Ar88kAW5oGk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Ar88kAW5oGk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

