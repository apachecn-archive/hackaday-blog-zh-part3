# Line Follower 有很多可回收的零件，但是没有大脑

> 原文：<https://hackaday.com/2017/03/18/line-follower-has-lots-of-recycled-parts-but-zero-brains/>

线追随者是一个久经考验的机器人类型；为了在明确定义的物理任务中取得成功，硬件和软件都需要协调工作。但是机器人并不总是有微控制器和软件，正如[马体 _DIY]的[零编程模拟线路跟随器](http://www.instructables.com/id/Simple-Line-Follower-Robot-With-No-Programming-Ana/)所展示的。

对于习惯于在几乎所有事物中看到 Raspberry Pi 或 Arduino 的读者来说，一个模拟机器人的“编程”只存在于其离散部件之间的和谐中，这可能是一个令人大开眼界且易于理解的项目。下面嵌入了机器人运行的视频。

[马体 _DIY]的设计使用两个 CNY70 反射传感器(本质上是红外发射器/光电晶体管对)和一个 LM358 双通道运算放大器。传感器一起充当两只近视眼睛。通过使用每个传感器的输出经由晶体管来驱动马达，黑线的存在与否直接且立即由所附马达的运动来反映。传感器看到的黑色越多，电机转得越多。电学上，这就是发生的一切；但是通过将右边的传感器连接到左边的电机上，将左边的传感器连接到右边的电机上，你会得到一个总是试图将黑线保持在传感器下方中心的机器人。玩弄电机和传感器的间距进一步调整性能。

 [https://www.youtube.com/embed/1kzXhrtN4sk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/1kzXhrtN4sk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[马体 _DIY]机器人中的电机看起来像 9g 伺服系统，但如果是这样，它们必须经过[修改才能连续旋转](http://hackaday.com/2008/07/14/modifying-a-servo-for-continuous-rotation/)才能在这种设计中工作。修改是一个经典的机器人黑客，但现在已经可以购买连续旋转格式的单位。

如果你觉得机器人学的这个方向很有趣，你可能会想看看我们多年来推出的各种光束机器人项目，比如[这个不倒翁](http://hackaday.com/2009/11/17/beam-robot-tumbles-aimlessly/)或者这个[太阳能涡轮混合动力](http://hackaday.com/2013/10/13/turbot-is-a-beampicaxe-hybrid/)。对于更复杂的无微控制器线路跟随器，一定要看看[这个看起来很光滑的机器人](http://hackaday.com/2016/09/27/line-follower-with-no-arduino/)，它具有 PID 的硬件实现。