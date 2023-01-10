# 平衡机器人需要创新的控制器和电机

> 原文：<https://hackaday.com/2017/05/18/balancing-robot-needs-innovative-controller-and-motor/>

自平衡机器人是学习控制理论和机器人学的好方法。机器人能够感知自己的位置和当前的环境，然后做出相应的反应来实现目标，这是所有机器人技术的关键。虽然业余机器人可能会使用廉价的伺服系统或有刷电机，但对于任何更先进的平衡机器人，你可能会想要使用[无刷 DC 电机和新的完全开源控制器](https://hackaday.io/project/21704-smoothcontrol)。

无刷 DC 电机的主要问题是它们在低速时表现不佳。为了克服这一缺点，市场上有大量专门的控制器可以帮助减轻他们的行为。到目前为止，所有这些控制器都已被锁定并成为专利。SmoothControl 正在寻求为这些电机创建一个完全开源的设计，它们看起来有一个很好的开端。该控制器被设计为运行在无处不在的 ATmega32U4 上，带有一个开源的三相驱动板。他们目前使用这些板和两个特定的电机，但计划随着项目的发展支持更多的电机。

我们之前已经看过详细说明为什么[无刷电机难以处理](http://hackaday.com/2015/04/20/driving-a-brushless-dc-motor-sloooooooowly/)的项目，所以为我们做这项工作的无刷 DC 电机的开源驱动程序似乎很有吸引力。除了机器人之外，无刷 DC 电机还有很多应用，像这样的控制器也很有用，[比如驱动飞机的螺旋桨](http://hackaday.com/2016/04/04/automating-rc-motor-efficiency-testing/)。