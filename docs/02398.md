# 手势玩俄罗斯方块

> 原文：<https://hackaday.com/2016/05/28/hand-gestures-play-tetris/>

有报道称，俄罗斯方块电影的预算相当可观，随之而来的是大量关于该如何运作的问题。角色会是谁？有什么样的线需要清理？无论答案是什么，我们都可以同时玩这个经典游戏。而且，多亏了康奈尔大学的一些工程学学生，[我们可以不用控制器来玩它。](https://people.ece.cornell.edu/land/courses/ece5760/FinalProjects/s2016/rjb297_map379_cs795/rjb297_map379_cs795/rjb297_map379_cs795/index.html)

这个黑客来自【Bruce Land】的 FPGA 设计课程。这个小组的游戏使用了一个摄像机，它输出一个标准的 NTSC 信号，并进行一些过滤来检测用户。从那里，用户可以将他们的手移动到屏幕的不同区域，从而控制俄罗斯方块的移动。这些信息通过 GPIO 发送到另一个 FPGA，FPGA 使用这些信息来玩游戏。

这个游戏完全是在硬件中完成的，这使得它相当独特。所有的游戏动态，包括方块生成、移动和边界条件都是在硬件中设置的，所有的皮肤识别也是在硬件中完成的。一定要看看学生们玩游戏的视频，如果你真的喜欢手势驱动的乐趣，你不仅仅局限于俄罗斯方块，[你还可以驾驶汽车](http://hackaday.com/2016/04/05/hand-gestures-drive-car/)。

 [https://www.youtube.com/embed/v-qqfSnmufg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/v-qqfSnmufg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

