# 胶带切割机器人修剪沉闷

> 原文：<https://hackaday.com/2017/10/06/tape-cutting-bot-trims-the-tedium/>

如果你曾经不得不组装一批电子套件，你会知道切割包含你的组件的胶带的乏味性质。数出四五个表面贴装电阻并用剪刀剪下一两次很容易，但当你面临重复这项任务一百次或更多次时，它的吸引力就开始变得苍白无力了。

[Overflo]在即将到来的德国 34C3 展会上为一个车间组装数百套套件时就遇到了这样的问题。解决办法？[当然是一个胶带切割机器人](https://www.youtube.com/watch?v=rFaoaCJ1R8o)！(YouTube 视频，嵌入下方。)

机器的核心是一把由步进电机操作的剪刀，它剪断由另一个步进电机传送的元件带。红外线光栅传感器计算链轮孔，整个过程由 Arduino Pro Mini 控制。一个特别聪明的技巧是，试纸经过一支记号笔，使得试剂盒中的不同成分可以通过颜色代码来识别。

这不是我们遇到的第一个解决这个问题的方法，这里有一个用激光切割元件带的方法。

 [https://www.youtube.com/embed/rFaoaCJ1R8o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/rFaoaCJ1R8o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[Nils Hitze]的提示。