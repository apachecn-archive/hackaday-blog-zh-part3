# 混合 3D 打印机创建完整的电路，外壳和所有

> 原文：<https://hackaday.com/2018/04/13/hybrid-3d-printer-creates-complete-circuits-case-and-all/>

这些天来，酷孩子似乎都认为我们正处于人工智能启示录的边缘，至少从花费在各种理论上的所有虚拟墨水来判断。但是，如果不能建造机器人军团来实施它们的意志，我们假定的人工智能霸主将很难接管世界。这就是为什么 3D 打印技术的进步可以整合电子电路，至少对某些人来说，可能有点可怕。

汉堡大学的 Florens Wasserfall 和他的同事们提出的基本想法是一台经过一些特殊修改的 3D 打印机。一个是喷射导电银聚合物墨水的独立挤出机，另一个是打印机挤出机上用于拾取和放置操作的简单真空头。打印机的底座还具有用于存储 SMD 部件的托盘和用于取放的照相机，以在将部件放置到未固化的导电油墨迹线中之前定位和定向它们。

不过，让硬件协同工作的关键是一个工具链，它允许电路集成到打印中。它从 Eagle 中的示意图开始，该示意图与开源切片包 Slic3r 的修改版本中要打印的零件的 CAD 模型相结合。SMD 元件的位置被确定，走线被确定，混合打印机一次构建整个组件。下面的视频展示了它的实际应用，我们不得不说它非常的巧妙。

当然，现在还只是学术上的，有简单的闪光电路之类的。但是把这个和类似于[这些 PCB 马达](http://hackaday.com/2018/01/24/this-tiny-motor-is-built-into-a-pcb/)的东西组合在一起，你就有了机器人噩梦的成分。或者不是。

 [https://www.youtube.com/embed/b0ta5CjxHSE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/b0ta5CjxHSE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[Simon Kühling]的提示。