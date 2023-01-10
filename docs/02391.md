# 动态 3D 打印和建模

> 原文：<https://hackaday.com/2016/05/17/3d-printing-and-modelling-on-the-fly/>

3D 打印应该是快速原型制作。设计、打印、使用、重新设计、打印、测试——直到满意为止。但是当你以 60 毫米/秒的速度放下细丝时，它看起来一点也不快。

[彭]、[吴]和他们在康乃尔大学的导师已经发明了一种[3D 打印机，它的打印速度几乎和你制作](http://www.huaishu.me/projects/on-the-fly.html)模型的速度一样快，并且能够在运行中对模型进行加减运算。我们的目标是快速制作出一个初始模型，这样设计和打印才能真正互动。他们看起来已经成功了——看看下面的视频。

3ders.org 有一篇关于这台机器的精彩报道，一旦这段视频的魔力消失，你也应该去看看。让这一切运转起来，还有很多事情要做。打印机增加了两个额外的自由度和一个刀头，这样它就可以从侧面进行加减操作，而不局限于一层一层的构造。为了让 ABS 冷却得足够快，以制成实心线，在打印后，喷水器会将 ABS 冷却到一定温度。

运行机器的软件也不可思议。当你把模型从机器上拉下来并测试它是否合适时，它能够暂停。然后恢复，就像什么都没发生一样。该部件连接到一个固定装置上——我们猜测它注册得很好——足以知道对象在哪里。CAD 软件还需要能够标记删除以及添加。甚至不要让我们开始路径规划的噩梦！

你可能会看着这些模型说它们看起来很粗糙。这是命中注定的——毕竟这只是一份草稿。这整个系统的运作是一个奇迹。在之前，我们已经写过关于[替代切片机的文章，甚至包括了](http://hackaday.com/2016/04/07/a-look-into-the-future-of-slicing/)[线框打印机](http://hackaday.com/2016/04/14/3d-cocooner-3d-lattice-printer/)，但是这个研究项目同时兼顾了两者。很酷的东西！

 [https://www.youtube.com/embed/X68cfl3igKE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/X68cfl3igKE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



谢谢[程]的提示！