# 由 HTML5 画布和 Java 网站控制的 Arduino Makerbeam Live 绘图仪

> 原文：<https://hackaday.com/2016/03/04/arduino-makerbeam-live-plotter-controlled-by-html5-canvas-and-java-website/>

我们从来没有见过有人用流行词来制作绘图仪，但是[roxen]在这方面做得非常好。想法很简单，把绘图仪放在一张纸上，打开一个网站，画图，看着绘图仪走。请看休息时间下面的视频。

用户绘制一个 HTML5 Canvas 对象，由 Java Web 服务器读取。从那里它被转换成 Arduino 的串行命令，Arduino 用两个 [EasyDrivers](http://www.schmalzhaus.com/BigEasyDriver/) 控制步进器。

这座建筑本身真不错。它完美地满足了笔式绘图仪的机械要求，没有很多绒毛。对于 x 轴和 y 轴，整个框架是 T 形的。机芯由两个步进器和乙缩醛齿条齿轮组产生。这支笔由一个业余爱好伺服系统上下升降。

我们喜欢使用橡胶端盖来保持框架与桌子的摩擦固定，并使用单个滚珠轴承来接触桌子的运动方向。这具有 3 点接触的额外好处，即自动将组件调整到纸张所在的同一平面。框架的任何扭曲都不会对它的绘图能力产生什么影响，因为它的末端效应器是一支圆珠笔。

我们真的很喜欢这个项目，并认为它会很有趣。你可以黑掉它，接受文本输入，并输出[笔迹](http://hackaday.com/2015/10/31/your-handwriting-is-now-your-font/)，如果你被一个不可信的机器人复制的你所取代，你会得到这个笔迹。

 [https://www.youtube.com/embed/Sn-WIluo1Us?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Sn-WIluo1Us?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢提示[丹尼尔 R.]！