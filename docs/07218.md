# 逆向工程吉他英雄

> 原文：<https://hackaday.com/2017/09/25/reverse-engineering-guitar-hero/>

当一个十年前的电子游戏有一个 bug 时，你会怎么做？如果你是[exile ord ],你可以修改它，即使你没有源代码。想知道怎么做吗？幸运的是，他制作了一个视频，展示了他如何找到并修复这个漏洞的所有细节。你可以看下面的视频。你可能关心也可能不关心吉他英雄，但是逆向工程和修补游戏的练习是逆向工程任何二进制软件，尤其是 Windows 二进制软件所需的工具和逻辑的一个很好的例子。

选择的工具是 IDA，一个交互式调试器和反汇编器。崩溃是一个例外，因为[ExileLord]以前在游戏上做过一些工作，他能够找到一个创建最终导致崩溃的屏幕元素的功能。

通过窥探虚拟桌子，他发现导致崩溃的物体。然而，他也发现对象的构造函数被复制保护方案所掩盖。然而，[流亡者]足够熟练地克服了晦涩的代码。

出现这个问题是因为文本对象是从预先分配的池中提取的。如果池运行为空，则无法创建更多池。修复？有几个，但是[ExileLord]只是增加了池的初始大小，这很好，除非你也打破了这个限制。

如果你想尝试这种工作，而你没有 IDA，你可以从一个在线的[反汇编工具](https://hackaday.com/2016/12/23/disassembly-required/)开始。它没有那么强大，但确实有效。不过，艾达非常能干，我们已经看到[在](https://hackaday.com/2013/10/14/reverse-engineering-a-d-link-backdoor/)之前使用过，效果很好。

 [https://www.youtube.com/embed/A9U5wK_boYM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/A9U5wK_boYM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

