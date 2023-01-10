# 25 行代码的微型编程语言

> 原文：<https://hackaday.com/2018/01/22/tiny-programming-langauge-in-25-lines-of-code/>

某些种类的程序让某些种类的软件黑客着迷。也许你对数字运算、国际象棋程序、操作系统或人工智能感兴趣。然而，在任何重要的机器上，大多数时候这些活动都需要某种语言。当然，我们都有一些处理器，我们可以在头脑中编写十六进制代码，但你真的希望至少有一个汇编程序，如果不是更坚固的东西。编写语言可能会上瘾，但直接进入 gcc 这样的大系统并试图做出改变对任何人来说都是令人生畏的。如果你想要一个温和的介绍，看看 25 行 Javascript 中的【mgechev 的】[语言。](http://blog.mgechev.com/2017/09/16/developing-simple-interpreter-transpiler-compiler-tutorial/)

GitHub 页面宣称它是一个微型编译器，尽管这有点误导，甚至 README 也说它是一个 transpiler。实际上，代码读取一种简单的语言，使用递归下降解析来构建一棵树，然后使用“编译器”将树转换为 JavaScript(当然，随后可以执行)。它也可以解释树并产生一个数字答案。

如你所料，如果你从文件中取出所有的注释，25 行的数字是。加上注释——它们是受欢迎的——它更像是 140 行代码。虽然内容不多，但它确实遵循了您对传统语言翻译系统的期望。也就是说，有一个词法分析器、一个解析器、一个解析树和解释或编译(类似于)代码的部分代码。

这可能不实际，但是很难想象还有比这更简单的例子。一旦你明白了它是如何工作的，你就可以继续构建你自己的语言。当然，您必须弄清楚一些事情，比如如何最好地解析代数表达式，以及如何处理解析冲突，但是您已经掌握了核心思想。

如果你认为你的老式电脑不需要花哨的传输器，你可能会感到惊讶。我们不确定 JavaScript 是否是我们编写这种东西的首选，但它无处不在，所以出于教育目的，它可能是一个不错的选择。此外，你可以将它[放在浏览器](https://hackaday.com/2012/04/10/html-based-avr-compiler-aims-to-make-arduino-development-on-ios-possible/)中(尽管，那篇文章[中的原始链接并没有移动](http://tadpol.org/projects/2012/02-02/AvrianJump.html))。