# 33C3:如果你不能信任你的电脑，你能信任谁？

> 原文：<https://hackaday.com/2016/12/29/33c3-if-you-cant-trust-your-computer-who-can-you-trust/>

这是一个时代的标志:第 33 届混沌通信大会(33C3)的第一天包括两个关于确保你自己的计算机不被用来对付你的会谈。这两个对话分别是现实的和理想的，在今天可以实现，并且是一个仍然处于想法阶段的作品。

在[第一次演讲](https://media.ccc.de/v/33c3-8314-bootstraping_a_slightly_more_secure_laptop)中，【Trammell Hudson】展示了他的[头像](https://github.com/osresearch/heads)开源固件引导程序和用于笔记本电脑和服务器的最小 Linux。这个名字是个笑话:Tails Linux 发行版让你操作时不留任何痕迹，而 Heads 让你运行一个你有理由确信是安全的系统。

它使用 coreboot、kexec 和 QubesOS，从根源上切断了基于 BIOS 的黑客工具。如果你担心粗略的 BIOS rootkits，这是一个解决方案。(而如果你认为这是偏执狂，你最近几年没有关注新闻，大概需要看一下这个演讲。)[Trammell]的 Heads distribution 是目前可用的最好工具的集合，它是你现在就可以做的事情，尽管它不会很容易。

实施在第二次会谈中充实的[想法更加困难——事实上，目前是不可能的。但这并不是说这不是一个好主意。[Jaseg]从 CPU 本身不可信这个前提出发。同样，遗憾的是，如今这并不那么遥不可及。非公开的固件比比皆是，如果你真的关心你的通信隐私，你不希望 CPU(或](https://media.ccc.de/v/33c3-8014-untrusting_the_cpu)[英特尔的管理引擎](http://hackaday.com/2016/01/22/the-trouble-with-intels-management-engine/))得到你的明文。

[Jaseg]的解决方案是在 CPU、屏幕和键盘之间插入一个设备，该设备可能由功能相当强大的 FPGA 制成，运行开源、可检查的代码。对于重要的文本，比如电子邮件，CPU 将只处理密文。通过图形提示，FPGA 将知道屏幕的哪个区域将被解密，并将明文直接发送到屏幕上。除非有人在 FPGA 和你的屏幕或键盘之间，否则这应该是不明显的。

和所有早期的想法一样，魔鬼将会在这里出现在细节中。例如，在将击键信息传递给 CPU 之前，如何知道键盘何时需要被编码还没有解决。但是这个想法非常有趣，它将信任边界尽可能地放在用户附近，在输入和输出处。