# 垃圾建筑打印机使用铅笔打印

> 原文：<https://hackaday.com/2018/01/31/junk-build-printer-uses-pencil-to-print/>

有时候，看看你能从你的垃圾抽屉里的碎片中构建出什么是很有趣的。West 博士]决定用包括硬盘、扫描仪底座和 Arduino 在内的备件制造一台打印机。结果是[一台相当酷的打印机，它用铅笔](https://www.youtube.com/watch?v=9ZrAjnPHzjQ)打印出图像，一次一个点地敲击图像。软件将图像转换成数组，0 代表白色，1 代表黑色。打印机本身的工作原理有点像老式的 CRT 电视:扫描仪阵列沿着一条水平线移动打印机，然后沿着另一条水平线垂直移动打印机。然后，如果该点的数组中有 1，它就会触发硬盘驱动器在纸上创建一个标记。

我们以前见过一些绘图打印机，但大多数使用绘图仪或 [CNC 方法](https://hackaday.com/2017/06/21/robot-draws-using-robust-cnc/)，其中电机在 X-Y 轴上移动铅笔。这种点阵打印机(有时称为[打点器](http://www.instructables.com/id/Doter-Huge-Arduino-Based-Dot-Matrix-Printer/))效率不高，但它很有趣，并显示了用一些垃圾和一些独创性可以实现的东西。

 [https://www.youtube.com/embed/9ZrAjnPHzjQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/9ZrAjnPHzjQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

