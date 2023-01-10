# 设计扁平柔性 PCB

> 原文：<https://hackaday.com/2016/05/05/designing-flat-flexible-pcbs/>

你几乎可以在每一件消费电子产品中找到柔性印刷电路板。这些层压在 Kapton 薄片中的铜的痕迹到处都是，设计这些电缆，更不用说制造它们了，对于车库电子向导来说是一种黑暗的艺术。制造这些扁平柔性电缆和印刷电路板仍然需要一些 Google-fu 或与工厂联系，但至少现在[设计这些电缆是一个解决的问题](http://oliver.st/blog/flexible-pcb-connections/)。

[Oli]需要一种方法通过移动部件将两块 PCB 连接在一起。通常这意味着某种连接器或电缆，但他开发了一种更好的解决方案——柔性 PCB 连接。为了生成夹在几层 Kapton 之间的这些铜迹线，[Oli]编写了一个 Python 脚本来获取一组参数，并为 Eagle 生成一个包括所有相关位的设计。

当然，对于灵活的 PCB 布局，问题是如何制造这些器件。我们已经看到一些有创造力的人[用 3D 打印机](http://hackaday.com/2014/10/28/make-flexible-pcbs-with-your-3d-printer/)制作柔性印刷电路板，并且[已经有不止一个 Hackaday Prize 项目](http://hackaday.com/2015/06/11/hackaday-prize-entry-flex-modules/)使用这些柔性印刷电路板。[Oli]说，任何柔性电路的制造商都应该能够毫不费力地复制从他的脚本中产生的一切。我们现在只需要奥什公园发明紫色 Kapton。

你可以在他的 GitHub 上抓取【Oli】的脚本[。](https://github.com/oliveroliver/ffsc-generator)