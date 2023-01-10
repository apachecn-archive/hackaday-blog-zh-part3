# 向前浏览

> 原文：<https://hackaday.com/2017/01/04/browsing-forth/>

Forth 在嵌入式开发人员中拥有强大的追随者。这有几个原因。几乎任何计算机都可以运行，甚至非常小的 CPU 都不适合运行用 C 编写的程序，更不用说托管一个成熟的开发环境了。本质上，Forth 非常简单。分析一个单词，在字典里查这个单词。词典要么指向某种机器语言代码，要么指向更多的单词。参数和其他东西一般都放在堆栈里。许多更高级别的 Forth 结构可以用 Forth 来表达，所以如果你的 Forth 系统达到一定的成熟度，如果你有足够的内存来吸收这些定义，它会突然变得非常强大。

如果你想尝试 Forth，你可能想在 PC 上开始学习它。有几个可以安装，包括 g forth(GNU 产品)。但有时这是一个障碍，必须安装一些复杂的软件，只是为了踢系统的轮胎。

我们现在有各种各样的其他应用程序在浏览器中运行，为什么不呢？毕竟，这个系统非常简单，用 Javascript 编写应该轻而易举。[Brendanator] [就是这么做的](https://www.npmjs.com/package/js-forth)，甚至还增强了 Forth 以允许与 Javascript 的互操作性。代码在 [GitHub](https://github.com/brendanator/jsForth) 上，但是真正有趣的部分是你可以打开[一个网络浏览器并使用 Forth](https://brendanator.github.io/jsForth/) 。

如果你想继续学习，你可以做得比从这里开始更糟。你也可以使用基于网络浏览器的 Forth 来尝试阅读。但是，如果你想创造你自己的 Forth，你真的应该读读[琼斯福斯](http://git.annexia.org/?p=jonesforth.git;a=tree)。它不仅是一个包含两个文件的 Forth 系统(一个汇编语言文件和一个 Forth 文件)，而且是我们见过的最好的[文化编程](http://hackaday.com/2016/06/06/learn-to-program-with-literate-programming/)的例子之一。

除了许多老式电脑和个人电脑之外，你还可以找到许多现代处理器。例如，我们已经看到了用于 [LPC ARM 芯片](http://hackaday.com/2015/08/30/go-forth-on-a-breadboard/)的系统。甚至还有一个版本的 [ESP8266](http://hackaday.com/2016/12/23/interactive-esp8266-development-with-punyforth/) 和 [Arduino](http://hackaday.com/2013/10/12/a-simple-forth-development-board/) (见下面第四个视频)。

 [https://www.youtube.com/embed/gFE6oK7jkq4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/gFE6oK7jkq4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

