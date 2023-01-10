# 我们现在可以 3D 打印紧身衣了

> 原文：<https://hackaday.com/2017/03/09/we-can-now-3d-print-slinkys/>

一台好的 3D 打印机的标志是层间附着力。如果 3D 打印的层离得太远，你会得到一个不好看的弱打印。[该印刷品无层间粘连](https://hackaday.io/project/20198-3d-printed-magic-spring)。这是一个 3D 打印的 Slinky，一个人或两个人滚下楼梯，发出 Slinky 的声音。传统观点认为，你不能打印一个 Slinky，但这并没有阻止[mpclauser]的尝试和成功。

这个小巧的模型是用几行输出 Gcode 文件的 JavaScript 代码制作的。没有。STL 文件，并且你不能在任何 CAD 工具中编辑这个 CNC Slinky。这也是异常怪异的 Gcode。根据[mpclauser]的说法，打印机在不断增加高度的同时，在内径和外径之间“曲折前进”。这是你期望从 3D 打印的 Slinky 中得到的刀具路径，但这也意味着普通的 Gcode 查看者在试图弄清楚如何显示这个东西时会感到不舒服。

生成你自己的 3D 可打印 Slinky Gcode 文件的所有代码都在[mpclauser]的 [Google Drive](https://drive.google.com/drive/folders/0B8DEuXB9wte4YnRVd2VBTU44ZjA?usp=sharing) 上。要看到这个打印结果，唯一的方法是下载 Gcode 文件并打印出来。开始吧。