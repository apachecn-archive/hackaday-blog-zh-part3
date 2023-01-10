# 机器人时钟一遍又一遍地写时间

> 原文：<https://hackaday.com/2015/10/06/robot-clock-writes-time-over-and-over-and-over/>

我们见过不少用钢笔或记号笔记时间的钟。如果你仔细想想，这真的不是一个很好的解决方案；每支白板笔都会在一两天内变干，即使你用的是钢笔，墨水最终还是会用完的。

[ekaggrat]想要一个没有这些问题的绘图时钟，在看了一眼磁性绘图板后，受到了启发。结果是一个时钟将永远写下时间。这是一个[的早期版本](http://hackaday.com/2012/03/14/robotic-doodle-clock/)的修订版，看起来更加可靠和机械精确。

写时间的钟需要某种不会退化的表面，但可以反复写入。白板和玻璃不行，任何有墨水的东西也不行。这个问题的解决办法是在“磁性书写板”或麦格纳涂鸦中找到的。这些磁性书写板有一系列包裹铁屑的小格。将一块磁铁放在纸板的一边，就会出现一点锉屑。将一块磁铁放在木板的另一面，锉屑就会消失。

[ekaggrat]的写时间机器人由一个小型的 Magna Doodle 显示器、一个由两个步进电机控制的机械臂和手臂末端的两个螺线管组成。运动学来自 RepRap 论坛上的一个有用的章节[，通过 ATmega644 和两个步进驱动器，这个时钟可以通过改变流经两个螺线管的电流来写时间。](http://forums.reprap.org/read.php?185,283327)

视频是体验这个项目的最佳方式，你可以在下面查看。

 [https://www.youtube.com/embed/MmIP156JIxg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/MmIP156JIxg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

