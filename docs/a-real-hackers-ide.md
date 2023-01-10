# 真正的黑客 IDE

> 原文：<https://hackaday.com/2017/04/17/a-real-hackers-ide/>

我们没有使用 GUI IDE，但如果我们使用了，它肯定会是类似于[马丁]的[嵌入式 IDE](https://github.com/martinribelotta/embedded-ide/wiki/usage-en)项目的东西。我们总觉得大多数 ide 只是我们使用的所有工具的花哨包装:Makefiles、`diff`、`git`、`[ctags](http://ctags.sourceforge.net/)`和编辑器。[Martin]的项目让它们不那么花哨，更加透明，更加可定制，同时保留了功能。这就是黑客的方式——将已经运行的经过验证的标准工具组合在一起。

他使用的代码编辑器是 [QScintilla](https://en.wikipedia.org/wiki/Scintilla_(software)) ，使用`[clang](http://clang.llvm.org/)`进行代码补全。新项目的“模板”系统？他使用`diff`和`patch`来导入和导出项目模板。因为它始终使用标准工具，所以您可以在类似 Ubuntu 的系统上用`sudo apt-get install clang diffutils patch ctags make`安装整个工具链。当然，您想使用的任何编译器都是受支持的。

我们看不到调试器界面，所以也许这是未来的事情？无论如何，如果你想要一个极简的 IDE，或者一个暴露它正在做的事情的内部工作而不是隐藏它们的 IDE，那么试试[Martin]的 IDE。如果你想要更多你无论如何都不会用到的功能，并且不介意有一点臃肿和晦涩，我们的许多作者都相信 Eclipse，包括 Arduino 平台和 T2 ARM 平台。我们会坚持我们的[蝴蝶](https://www.xkcd.com/378/)。