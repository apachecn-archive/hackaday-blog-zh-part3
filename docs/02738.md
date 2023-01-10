# 树莓派零成为强大的微型《我的世界》机器

> 原文：<https://hackaday.com/2016/07/02/raspberry-pi-zero-becomes-mighty-miniature-minecraft-machine/>

在一次巧妙的小型化中，[JediJeremy]几乎完成了树莓派 Zero 的[陀螺鼠标控制器](http://unorthodox-engineers.blogspot.com.au/2016/06/pi-manipulator-build-part-1.html)！最终，这将是一款可穿戴的 Linux 手表，但在这个过程中，他在界面上获得了一些乐趣。

使用四轴飞行器的 MPU6040 陀螺仪/加速度计卡，[JediJeremy]花了一周时间编写驱动程序，让它可以像鼠标一样工作。用橡皮筋将 Adafruit 1.5”PAL/NTSC LCD 屏幕及其驱动板捆绑到零，使其成为我们见过的最小功能计算机和屏幕组合之一。简单地倾斜整个东西来引导光标。

它目前没有任何键盘输入，而且[JediJeremy]只增加了一个点击按钮，但是看看这个东西！它太小了！用他自己的话说:“我认为这是第一台我可以不小心洒到咖啡里的电脑，而不是相反。”

 [https://www.youtube.com/embed/fJKJoDHDHiA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/fJKJoDHDHiA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



在此过程中出现了一些问题。他原本计划使用加速度计检测屏幕上的点击，并将其用作点击输入，但这扰乱了光标的位置。屏幕的驱动板也喜欢过热，因为屏幕不会完全关闭，所以它往往会延长电池寿命——但它仍然是概念的功能证明。

剥去对笨拙鼠标的需求，与这台高效的计算机保持完美的主题一致。最好的部分是所有组件的极低价格点，因此构建自己的组件也是一个具有成本效益的项目！如果这不合你的口味，为什么不用一个按钮来播放《辛普森一家》的随机一集呢？

[via [/r/raspberry_pi](https://www.reddit.com/r/raspberry_pi/comments/4p3x6x/gyromouse_demo_smallest_gui_in_the_world/)