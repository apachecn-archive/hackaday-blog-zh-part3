# 反齿槽算法带来了你的爱好无刷电机最好的

> 原文：<https://hackaday.com/2016/02/23/anti-cogging-algorithm-brings-out-the-best-in-your-hobby-brushless-motors/>

廉价的无刷电机可能是这些天我们的遥控飞机和四轴飞行器背后的主力，但我们从未在任何需要低速精度的应用中见过它们。为什么？遗憾的是，廉价的无刷电机的机械结构不够好，无法提供精确的位置控制，因为它们会表现出齿槽转矩，这是一种意想不到的电机特性，会导致输出转矩因转子位置而略有变化。马修·皮考利(Matthew Piccoli)和宾夕法尼亚大学 ModLab 的同事们毫不气馁，已经开发了两种方法来补偿和最小化扭矩波动(T1 ),从本质上使廉价的 BLDC 电机具有与其价格更高的同类产品相当的性能。更重要的是，他们已经证明了他们的算法在硬件中的有效性，他们用无刷电机建造了一个涂鸦的直接驱动机械臂，可以跟踪轨迹。

齿槽转矩是位置的函数。[Matthew's]算法的工作原理是测量将转子伺服到一整圈中每个可测量的编码器位置所需的外加电压(或电流)。齿槽转矩是有方向的，因此这个“电机指纹”需要在两个方向上都取。通过记录所有可测量位置的这些测量电压(或电流),补偿齿槽转矩只需在驱动电机时减去任何给定位置的测量值。[Matthew]在他的论文中不厌其烦地详细描述了这些微妙之处，他实际上开发了一种额外的基于加速的方法。

霍比 BLDC 汽车公司如今比比皆是，你甚至可能有一些备件藏在货架上。这种算法应用于电机控制器电子设备时，可以让我们有机会重新审视那些要求高扭矩精确电机控制的项目——这是我们只有在买得起几台马辰电机的情况下才能梦想的事情。如果你是 BLDC 电机控制理论的新手，看看过去的几个[项目，让自己开始运行。](http://hackaday.com/2016/02/04/adding-position-control-to-an-open-source-brushless-motor-driver/)

 [https://www.youtube.com/embed/Rp8YyCMY4vs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Rp8YyCMY4vs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

