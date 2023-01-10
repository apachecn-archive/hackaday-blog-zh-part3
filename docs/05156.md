# DIY 3D 切片机是一台发电机

> 原文：<https://hackaday.com/2017/03/01/diy-3d-slicer-is-a-dynamo/>

我们都知道黑客不会使用常规编译器。如果他不用汇编语言，他就用自己写的编译器。如果你不认识他，也许就是你！如果你真的不认识一个，那就认识这两个。[Nathan Fuller]和[Andy Baldwin]希望鼓励你编写自己的 3D 切片器。

他们的帖子非常详细，并且使用 Autodesk Dynamo 作为图形编程语言。然而，细节并不是迪纳摩特有的。它就像一个编译器。你大概知道它必须做什么，但是在你看到它被拆开之前，如果你从头开始构建它，你可能不会马上想到许多微妙之处。

切片器必须确定 3D 模型的每个切片看起来像什么，并创建 Gcode 来表示这些层。然后，Gcode 驱动打印机。为什么要构建自己的切片器？在我们做这种事情之前，我们从来不需要理由。但是如果你坚持的话，想想你自己的切片器如何允许你试验不同类型的支撑结构生成、填充图案和其他细节。

当然，许多切片器都是开源的，所以您也可以从那里开始。然而，这些通常都是功能齐全的成熟产品，很难弄清楚如何将自己的代码插入其中(编写 Cura 插件可能是个例外)。

我们之前已经讨论过像[可变高度层](https://hackaday.com/2017/02/16/hands-on-with-variable-layer-height/)这样的切片技巧。我们还谈到了使用脚本语言来[管理来自切片器](https://hackaday.com/2016/07/20/3d-printering-g-code-post-processing-with-perl/)的 Gcode 输出。我们甚至有自己的工具[来合并不同选项(比如图层高度)的 Gcode](https://hackaday.com/2015/07/22/better-3d-prints-by-mixing-slicing-techniques/) 。当谈到切片时，你喜欢使用什么技巧？

感谢[smerrett79]指出这一点。