# 自动建模的 Tinkercad 编码技巧

> 原文：<https://hackaday.com/2018/07/06/tinkercad-coding-tricks-to-automate-modeling/>

如果你想快速设计 3D 打印，Tinkercad 非常容易使用。尽管它曾一度面临倒闭的危险，但它被 AutoDesk 收购了，AutoDesk 对其进行了大量改进。在同一个工具中编程和模拟 Arduino 是可能的——这总是给我们一种奇怪的并列感。然而，[Chuck]在下面的视频中向我们展示了如何使用相同的代码块来自动化 Tinkercad 3D 建模，这要归功于软件中的测试功能。可以把它想象成浏览器中基于 GUI 的 OpenSCAD。

你必须开始一个 Codeblocks 项目，当你这样做时，你可以选择一个初始设计，或者只需按下新设计的按钮，就可以得到一个空白的石板。这些块看起来像其他与 Scratch 相关的编程语言。您可以创建变量、重复命令组和创建项目。[Chuck]提到启动代码中没有注释，这是一个合理的批评。你可以使用一个注释块。

许多块有一个箭头，使他们扩大，所以你可以看到所有不同的参数。这使得代码更容易阅读，比其他方式更紧凑。大部分都很容易弄清楚，但似乎没有太多的文档。例如，我们花了一段时间才意识到立方体块上的“边缘”是边缘有多圆。

当然，像任何语言一样，你可以聪明地使用它，也可以愚蠢地使用它。在顶部设置参数，并像示例那样从中导出测量值，这无疑是一个最佳实践。仅仅输入数字只比使用传统的 GUI 好一点点。注意，你不能在平面设计和区块之间来回翻转。但是，您可以将结果导出为 Tinkercad 部件，以便在常规设计中使用。

我们喜欢[Chuck]以正常方式画出一张表格，然后展示用积木画出表格的优势。我们总是讨厌这些块语言，比如说，从一个循环中删除一个块是多么困难。你必须抓住你想要删除的块并移动它，这也移动了它下面的所有东西。然后第二次移动该方块下的所有方块，将其放回原处。然后，您可以删除新孤立的块。工作太多了！

我们希望看到一些我们以前在 Tinkercad 中看到的类似于这样的[准参数化的东西](https://hackaday.com/2018/04/23/parametric-hinges-with-tinkercad/)。另一方面，如果你不介意安装软件，总会有 [SolveSpace](https://hackaday.com/2016/06/18/solvespace-a-parametric-cad-tool/) 。

 [https://www.youtube.com/embed/FlsmkPCYIzc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/FlsmkPCYIzc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

