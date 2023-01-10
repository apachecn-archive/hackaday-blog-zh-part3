# 充气管阵列的冒险

> 原文：<https://hackaday.com/2018/04/25/adventures-in-gas-filled-tube-arrays/>

真空管很牛逼，Nixies 更牛逼。纳米管是新的热点，但有一种类型的管比所有其他的都好。是игг1-64/64M。这是一个 64×64 网格的电子管面板，有些只有绿点，有些有绿色和橙色，甚至还有红、绿、蓝 64×64 像素矩阵。它们要么是荧光粉，要么是充气管，但这是所有电子管显示器中的王者。即使是大屏幕中的 RGB 显像管也比不上这种显像管阵列的荒谬。

[Muth]拿到了一些面板，[最后他在上面显示图像](https://hackaday.io/project/46302-1-64x64m-adventure)。这是一个令人惊叹的项目，包括查找文档、翻译文档、用 360 伏电压驱动电子管，以及想出一种方法，只用几个微控制器引脚就能驱动 128 路输入。

第一，电源。这些面板需要大约 360 伏的电压才能点亮。这明显高于通常在谢妮钟或其他普通电子管显示器中发现的数值。这不成问题，因为仔细阅读数据手册就会发现，有一个电路可以将正常的 180 伏谢妮电源提高到适当的电压。为了驱动这些像素，[Muth]采用了一个相当大的 PIC18F 微控制器，带有八个三态缓冲器。微控制器通过串行端口接收数据，并扫描整个帧缓冲区。总之，有 8 个驱动板、736 个元件和 160 根电线将一切连接在一起。这需要大量的工作，但现在[Muth]有了一个 64×64 的显示器，它是绿色的*和橙色的*。

你可以在下面查看这款显示器的“pixel dust”演示。

 [https://www.youtube.com/embed/ZqoKS0ZieYE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ZqoKS0ZieYE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

