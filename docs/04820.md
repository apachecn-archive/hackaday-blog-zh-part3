# 运算放大器组合成盒子里的虚拟球

> 原文：<https://hackaday.com/2017/01/28/op-amps-combine-into-virtual-ball-in-a-box/>

把球扔进盒子里会发生什么？在现实世界中，答案很简单——球在墙壁和地板之间反弹，直到它最终失去能量并停止运动。当你把一个虚拟的球扔进一个虚拟的盒子里会发生什么？听起来你可能需要一个运行在数字计算机上的程序来回答。但是用几个运算放大器构建的模拟计算机也可以很方便地在盒子里模拟一个球。

好吧，在这个简单的系统中建模需要相当多的运算放大器和相当大的聪明才智，正如[格伦·克莱恩施密特]在着手重建 AEG-特勒芬肯公司一个 40 年之久的演示项目时发现的那样。绘制在虚拟框内反弹的对象的位置是两个独立电路的工作，一个用于确定 Y 坐标并从地板上反弹，另一个用于计算相对于墙壁的 X 坐标。这些电路由一个高频正弦余弦对发生器叠加而成，产生一个球，所有的东西混合在一起，形成单独的输出，供 X-Y 示波器显示。由此产生的模拟非常令人信服，每次墙壁被击中时，用于改变 X 方向的继电器缓慢衰减的咔哒声是额外的奖励。

虽然没有太多实际用途，但肯定具有指导意义，并且令人印象深刻地展示了运算放大器的潜力。有关将运算放大器用作模拟计算机的更多信息，请查看[【Bil Herd】的“模拟计算”](http://hackaday.com/2014/07/25/bil-herd-computing-with-analog/)文章。

 [https://www.youtube.com/embed/9dw3aDMlCso?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/9dw3aDMlCso?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[Frank]的提示，并帮助[Glen]修补不可靠的谷歌翻译。