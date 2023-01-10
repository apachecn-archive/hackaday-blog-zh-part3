# 逆向工程 ST-Link 程序员

> 原文：<https://hackaday.com/2016/12/10/reverse-engineering-an-st-link-programmer/>

我们不确定*为什么*【lujji】想要黑掉 ST 的 ST-Link 编程器固件，但他这样做肯定很酷，他的文章是黑掉嵌入式设备的一个很好的入门，分为两部分:首先他[解包并解密工厂固件](https://lujji.github.io/blog/reverse-engineering-stlink-firmware/)并验证他可以通过引导加载程序上传自己的加密固件，然后他转储引导加载程序，找出它锁定固件映像的位置，然后[避开保护](https://lujji.github.io/blog/reverse-engineering-stlink-firmware-part2/)。

[从【Taylor Killian】之前的工作中获得了固件的加密密钥](http://www.taylorkillian.com/2013/01/retrieving-st-linkv2-firmware-from.html)，这极大地帮助了【lujji】的项目。一旦能够在一个完整的设备上运行自己的代码，[lujji]编写了一个快速的例程，将整个闪存 ROM 的内容通过串行端口转储出去。这为他提供了引导加载程序二进制文件，这是两部分拼图中缺失的一块。

如果你曾经打破过 20 世纪 90 年代中期的版权保护，你不会对接下来发生的事情感到惊讶。[lujji]找到了引导程序添加读保护的例程，并取消了它。用这个修改过的引导程序上传固件后，[lujji]发现它不再是读保护了。游戏结束！

我们一路上忽略了一些有用的提示和技巧，所以如果你喜欢逆向固件，可以看看[lujji]的博客。然而，如果你只是想要一个具有 UART 功能的好的 ARM 程序员，没有理由走这些极端。[黑魔法探测器](http://hackaday.com/2016/12/02/black-magic-probe-the-best-arm-jtag-debugger/)项目给你同样的功能，而且它是开源的。或者考虑到官方的 ST-Link 程序员几乎免费赠送每一个 Nucleo 板，购买一个显然是阻力最小的途径。但是像这样一个好的黑客对那些想走这条路的人来说是一种奖励。谢谢你写了它。