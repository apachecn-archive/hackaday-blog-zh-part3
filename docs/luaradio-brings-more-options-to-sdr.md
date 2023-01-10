# LuaRadio 为 SDR 带来更多选择

> 原文：<https://hackaday.com/2016/07/06/luaradio-brings-more-options-to-sdr/>

GNURadio 是软件定义无线电套件的瑞士军刀:它无所不能。它有一个很棒的 GUI 覆盖层，使得创建无线电流相当简单。整个系统只有两个地方我们可以挑剔——这是一套庞大的软件，用 Python 编写代码比使用 GUI 要难得多。

[万尼亚·谢尔盖耶夫]启动了他的 Lua radio 项目来解决这些缺点。如果你在寻找全 GUI 体验，那你找错人了。LuaRadio 的目标是使事情易于编码，并保持代码库小而整洁。

然而，这并不意味着它完全背离了 GNURadio 非常成功的流程图编程范例，如果您熟悉将信号源连接到滤波器模块再连接到输出的过程，您在这里也会做得很好。看看[必不可少的 FM 收音机演示](http://luaradio.io/examples/rtlsdr-wbfm-mono.html)——SDR 的“hello world”——你会看到它是如何工作的:在代码中实例化各种块，然后发出“connect”命令将它们链接在一起。

LuaRadio 的主要卖点是它的尺寸和手工编程的便利性。它有[伟大的文档](http://luaradio.io/docs/reference-manual.html)来启动。它被写成一个库，可以嵌入到你的 C 代码中[，这样你就可以编写独立的程序来利用它的功能。](http://luaradio.io/docs/embedding-luaradio.html)

LuaRadio 是一个新项目，它也没有 GUI。如果你害怕打字，这可能不是 SDR 的理想入门。(如果你是 SDR 新手，[从这里开始](http://hackaday.com/2016/05/30/hackaday-dictionary-software-defined-radio-sdr/)。)但是如果你想通过*编码*来编码你的 SDR，或者在更小的设备上运行你的收音机，它可能值得一看。它的版本是 v0.1.1，所以我们期待在未来听到更多来自 LuaRadio 的消息。你们有人用吗？我们很想在评论中听到。