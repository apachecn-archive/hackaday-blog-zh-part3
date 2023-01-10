# 利用红外技术改善机器人的室内导航

> 原文：<https://hackaday.com/2018/06/27/improving-indoor-navigation-of-robots-with-ir/>

如果 CES 上的展位是可信的，未来充满了家用机器人:从有轮子的人形机器人到用胶带粘在 Roomba 上的 Alexas 管道机器人。回到现实，家用机器人真的还不是一个东西。这有一个显而易见的原因:在房子里走动很困难。机器人可能真的需要腿来上下楼梯，而 GPS 在室内根本不存在，至少达不到所需的精度。机器人究竟是如何在室内导航的？

这个 Hackaday 奖的项目解决了室内导航的问题，而且它以一种令人惊讶的巧妙方式解决了这个问题。这是用二维码导航，但不是随便什么二维码。它们是由红外摄像机读取的二维码，用一种特殊的人眼不可见的红外敏感涂料涂在墙壁和天花板上。这是机器人视觉导航，这是一个奇妙的想法。

这个项目背后的基本想法是使用一个红外摄像头——或者基本上是任何去掉红外阻挡滤波器的网络摄像头——和大量的红外发光二极管来照亮任何目标。到目前为止，概念证明是有效的。计算机可以很容易地读取二维码，如果颜料对于人眼是不可见的，但是对于红外照相机是可见的，那么整个项目仅仅是一个实施的问题。

已经有很多项目尝试给机器人增加室内导航功能。他们有的用激光雷达，有的用计算机视觉和 SLAM。这些在计算上是昂贵的。一些人甚至使用无线信标在室内导航[，就像 2016 年黑客日大奖](https://hackaday.io/project/9242-subpos-ranger)中的 SubPos Ranger 一样。使用红外和二维码是如此简单和黑客友好，我们认为这太棒了。

The [HackadayPrize2018](https://hackaday.io/prize) is Sponsored by: [![Microchip](img/20eb9d92b47da4c15177567c02a65727.png)](https://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey)  [![Supplyframe](img/2d012d9fc9c7873688699aeadb4742d2.png)](https://supplyframe.com/)