# 使用 GCC 开发 MSDOS

> 原文：<https://hackaday.com/2018/05/14/msdos-development-with-gcc/>

在 2018 年考虑 MSDOS 中的编程可能看起来很奇怪。但是，如果你是老式计算机爱好者，或者必须用 MSDOS 单板计算机支持一些旧设备，它可能就是你要的东西。问题是，你从哪里得到一个不用在古老的 DOS 机器上运行的有效的编译器？事实证明，gcc 可以做到这一点。[蕾妮·蕾贝]根据[克里斯·韦隆斯]的博客文章为[提供了一个视频演示](https://www.youtube.com/watch?v=Y7vU5T6rKHE)。你可以看下面的视频。

该技术生成 COM 文件，而不是 EXE 文件，因此有一些限制，例如 64K 的文件大小。编译器也不会为任何低于 80386 的 CPU 生成代码，所以如果你有一个真正的 8086、80186 或 80286 CPU，你就不走运了。生成的代码将在 386 或更高版本的真实 DOS 环境中运行，或者在类似 DOSBox 的模拟器中运行。

你可能会想为什么不用 gcc 的 DJGPP 端口来连接 DOS 呢？这听起来不错，但它实际上不会产生真正的 DOS 代码。它为 DOS 扩展程序生成代码。此外，[Chris]很难让它与现代系统配合工作。

这里唯一真正的技巧是使用正确的 gcc 标志组合，用正确的代码创建一个独立的图像。COM 文件只是一个内存转储，所以你不需要一个花哨的头文件或任何东西。当然，你也没有任何库支持，所以你必须写所有的东西，包括函数，比如说，在屏幕上打印。当然，如果你喜欢，你可以借[克里斯的]。

这个难题的最后一部分包括添加一个小存根来设置和调用 main，并让链接器输出一个最小文件。一旦你有了这些，你就可以像 1993 年一样编程了。不要错过[第 2 部分](https://www.youtube.com/watch?v=EXiF7g8Hmt4&feature=youtu.be)，它涵盖了中断。

如果你渴望 QuickBasic 而不是 C，[去下载这个](https://hackaday.com/2018/02/22/quickbasic-lives-on-with-qb64/)。如果你只是想运行一些旧的 DOS 游戏，那么[就像你的浏览器](https://hackaday.com/2016/02/05/a-dos-education-in-your-browser/)一样近。

 [https://www.youtube.com/embed/Y7vU5T6rKHE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Y7vU5T6rKHE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

