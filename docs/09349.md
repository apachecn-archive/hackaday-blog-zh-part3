# 让老式计算变得简单，困难重重

> 原文：<https://hackaday.com/2018/05/04/making-vintage-computing-easy-the-hard-way/>

如果你不想想当然地认为计算机已经变得如此简单和无缝，那就把老式计算作为一种爱好。如果你冒险走上复古之路，你会很快质疑任何人是如何用计算机完成有用的工作的，你在计算机历史上越往前追溯，一切似乎变得越困难。

一个典型的例子:你如何在自制的 PC/XT 和你的现代台式机之间轻松地传输文件？过去，我们用零调制解调器电缆或运动鞋网堆叠的软盘来实现这一点，但[斯科特·m·贝克]找到了另一种方法——在 ISA 总线上放置一个 Raspberry Pi 作为虚拟软盘驱动器。ISA 卡的核心是 IDT7130，这是一个 kb RAM 芯片，允许通过双端口进行同步异步访问。一个端口与 ISA 总线通信，另一个端口与 Pi 的 GPIO 通信，当然是在电平转换后，使所有的电压都兼容。[Scott]为该卡编写了一个驱动程序，将一个 Pi Zero W 插入头部引脚，并组装了一个 Python 服务器，使本地图像可用于卡上的共享内存。这样做的结果是，复古机以为里面有软盘，其实是服务器。下面的视频有大量的细节，并显示了卡的行动。相当狡猾。

[斯科特]的项目总是很有趣，他似乎真的有复古生活拨入。无论是[老点唱机黑客](https://hackaday.com/2018/03/30/this-is-how-the-fonz-would-play-mp3s/)还是【Z80s 的 Unix 操作系统，都有很多东西要学。虽然我们希望在视频中看到更多关于 PC/XT 的信息；我们在前面板上看到的是 Nixies 吗？

 [https://www.youtube.com/embed/eDD2GbaMwYA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/eDD2GbaMwYA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

