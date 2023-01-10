# 实时 FPGA 手指检测

> 原文：<https://hackaday.com/2016/06/04/real-time-fpga-finger-detection/>

从[Bruce Land]的微控制器和 FPGA 编程课程中出来的学生项目在这里有很多特色，很简单，因为其中一些非常棒，但也因为每个项目都是另一个项目的基础。我们希望它们会适合你。

这一次，[阴军·陈]和[杨子奇]创造了一个五排游戏，由一个手指控制[。指向屏幕的摄像机拍摄玩家的手，并将 VGA 数据传递给 FPGA。这就是事情变得有趣的地方。](https://people.ece.cornell.edu/land/courses/ece5760/FinalProjects/s2016/jc2954_zy259/jc2954_zy259/jc2954_zy259.html)

FPGA 中的算法检测皮肤颜色，在几次打开和关闭操作后，得出一个非常好的手部轮廓。指尖定位相当巧妙。它们将 X 轴和 Y 轴上检测到的像素数量相加，由于手指细长，因此定位指尖，因为它将在一个轴上具有最大值，而在另一个轴上具有最小值。甜甜的(虽然玩家要穿长袖才能完美发挥作用)。

摄像头怎么拍不到后台正在进行的游戏？他们使用黑白游戏场，而肤色检测完全忽略了这一点。而游戏本身运行在 FPGA 中的一个 [Nios 嵌入式处理器](http://wl.altera.com/devices/processor/nios2/ni2-index.html)中。在项目页面上有更多的细节，当然下面还有一个演示视频。

我们喜欢听兰德教授的课。他的[视频系列](https://www.youtube.com/user/ece4760/playlists)是非常宝贵的，课程项目一直是一个灵感。

 [https://www.youtube.com/embed/2rWrv-5ZufY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/2rWrv-5ZufY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

