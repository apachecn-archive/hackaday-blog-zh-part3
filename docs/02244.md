# 带有步进器的简单机器人手臂具有令人愉快的平滑运动

> 原文：<https://hackaday.com/2016/05/02/simple-robot-arm-with-steppers-has-pleasingly-smooth-motion/>

当[建造一个简单的机器人手臂](http://www.bajdi.com/mearm-forked/)时，通常的做法是无处不在的业余爱好伺服。然而，这些设备并不精确，并且通常不稳定和不可靠。他们有自己的优势，但如果不需要力量，步进电机将在相同的价格范围内提供更好的运动。

当[Bajdi]设计出 [Mearm projec](http://hackaday.com/2015/07/31/human-gestures-control-this-robot-arm/) t 并将其用于小型步进电机时，他就是沿着这些思路思考的。首先，他尝试在 thingiverse 上打印出[伺服版本](http://www.thingiverse.com/thing:616239)。它工作了，但零件对于 3D 打印来说并不理想，而且他不喜欢这个运动。

所以他购买了一些 28BYJ-48 发动机。这些都是微小的齿轮步进器，往往会出现在奇怪的项目。他修改并简化了 FreeCAD 中的文件。随着 CNC 防护罩和 Arduino 的加入，他拥有了升级所需的一切。伺服系统现在仅用于夹持器。

几乎可以肯定，机器人的有效载荷能力较弱，但正如你在休息后的前后视频中看到的那样，它明显更流畅、更准确。

 [https://www.youtube.com/embed/y2PD51d_DRg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/y2PD51d_DRg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/TdO51ApYu1U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/TdO51ApYu1U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

