# 用 3D 打印机制作焊接模板

> 原文：<https://hackaday.com/2016/02/08/solder-stencils-with-a-3d-printer/>

如果你用锡膏焊接，模板会让事情变得简单很多。当然，你可以用注射器手工涂膏，但是现代 PCB 可能有数百甚至数千个焊盘。像我们许多人一样，[罗伯特·克伯里奇]不喜欢花钱制作模板，他想知道是否可以用他的 3D 打印机来制作模板。他发现[的答案是肯定的](https://hackaday.io/project/9550-solder-stencilme)。

[Robert]使用热板进行焊接，使用 Python 构建应用程序，将两个 Gerber 文件转换为 STL，这将使您的打印机生成可工作的模板。显然，模板的厚度必须至少达到打印机的最小层高。如果您使用 Eagle，[Robert]有一个脚本可以帮助您，但是电路板轮廓和粘贴层的任何 Gerber 文件都应该可以工作。

你可以在 [GitHub](https://github.com/kirberich/gerber_to_scad) 上找到这些文件，也可以在[网站](http://solder-stencil.me/)上使用这个应用程序。Python 代码将 Gerbers 转换成。由 OpenSCAD 处理的 scad 文件。如果你喜欢锡罐胜过塑料，[我们已经为你准备好了](http://hackaday.com/2013/07/02/the-definitive-guide-to-solder-stencils/)。如果你喜欢，你甚至可以使用啤酒罐。如果你以前没有用过焊料模板，你可能会喜欢下面来自 SparkFun 的视频。

 [https://www.youtube.com/embed/WDIqtGMROjM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/WDIqtGMROjM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

