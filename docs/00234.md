# 树莓派哨兵炮塔是全人类的敌人

> 原文：<https://hackaday.com/2015/10/03/raspberry-pi-sentry-turret-is-the-enemy-of-all-mankind/>

战争，嗯，有什么好处？绝对没有，除了作为一个借口[建造一个树莓派动力的哨兵炮塔](https://github.com/matt-desmarais/SentryTurret/)来追踪并向你的敌人开火。这就是[马特·德马里斯]决定要做的，他已经公布了他的构建的全部细节。

它缺乏大多数军事硬件的优雅，但你还能指望一个快速而肮脏的黑客呢？它既不闪亮也不不祥，但它有致命的运动跟踪功能。[Matt]正在使用 OpenCV 来检测 USB 网络摄像头的移动，两个伺服系统来平移和倾斜摄像机和枪，以及一个小型继电器来扣动扳机。也可以对网络间进行手动控制。

我们已经看到了许多类似的使用武器的构建，如[橡皮筋](http://hackaday.com/2015/08/13/arduino-powered-rubber-band-sentry-turret-is-not-a-lie/)和 [Nerf 枪](http://hackaday.com/2010/06/18/nerf-sentry-turret/)，但是如果你有兴趣看看如何将 OpenCV 和 servos 等工具结合在一起，以创建一个主动跟踪运动的相机，这是一个很好的开始。