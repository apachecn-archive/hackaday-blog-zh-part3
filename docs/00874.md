# 球平衡 Arduino 风格

> 原文：<https://hackaday.com/2015/12/14/ball-balancing-arduino-style/>

如果你有很好的平衡感，你可以骑独轮车或者上电视用梯子做特技。我们不知道[Hanna Yatco]是否有良好的平衡感，但我们知道她的 Arduino 有。她的建造使用了无处不在的 HC-SR04 声纳传感器和伺服系统。

这是一个伟大的使用伺服，因为一个标准的伺服电机没有修改只通过一个圆的一部分，这就是这个项目所需要的。PID 算法测量到球的距离，并升高或降低光束以试图使球到达中心。

像这样的伺服系统通常在无线电控制的车辆中运行，它们非常容易驾驶。耦合到轴的电位计产生一个脉冲，伺服系统在内部将该脉冲与来自微控制器的脉冲进行比较。如果脉冲比参考脉冲宽，电机向一个方向驱动。如果脉冲比参考脉冲窄，电机以另一个方向运行。它驱动多少取决于两个脉冲之间的差异有多大。当脉冲匹配时，伺服电机停止运动。从 Arduino 或其它微控制器的逻辑输出驱动这种脉冲排列非常简单。

建造细节有点稀疏，但你可以在视频中看到总体布局，如果你想了解更多细节，她链接到一个启发了这个的类似项目。

如果你更喜欢，你可以在[二维空间做同样的把戏。或者也许你想尝试使用一个](http://hackaday.com/2014/08/22/stewart-platform-ball-bearing-balancer/)[飞行时间传感器](http://hackaday.com/2015/02/14/ball-balancing-robot-uses-new-tof-sensor/)。

 [https://www.youtube.com/embed/9pj93-uGIUo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/9pj93-uGIUo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

