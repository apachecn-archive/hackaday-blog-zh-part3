# 用打字机键盘制造一些噪音

> 原文：<https://hackaday.com/2017/07/16/make-some-noise-with-the-typewriter-keyboard/>

你是一个愤怒的程序员吗？在完成每一行代码后，你是否经常有想按回车键或空格键的冲动？那么，康斯坦丁·肖维克的[打字机键盘](http://www.konstantin-schauwecker.de/typewriter.php)正适合你。在他的项目中，[康斯坦丁]将一台德国奥林匹亚莫尼卡打字机黑进了 USB 键盘。

该项目使用了不少于 50 个安装在定制 PCB 上的光电断路器，PCB 直接安装在打字机本身的下方。电路板是这样设计的，锤臂在阻挡光遮断器时占据一个位置。每次按下一个键，相应的设备就会向 Arduino 发送一个信号。

为了能够将 50 个信号连接到 Arduino Leonardo，采用了多路复用器和解码器。CD4515，4×16 线路解码器用于激活光信号，CD4067，16×4 多路复用器用于返回扫描。这形成了传统的扫描键盘矩阵，整个事情都在 Arduino 代码中管理([作为 zip 文件](http://www.konstantin-schauwecker.de/files/schreibmaschine.zip)提供)。

对于那些想黑掉他们爷爷的旧打字机或者做一台来惹恼坐在他们旁边的家伙的人来说，这个项目可以是一个很好的起点。看看下面的视频演示和拆卸，如果你喜欢树莓 Pis，那么看看这个机械打字机黑客。

 [https://www.youtube.com/embed/g8Sm4_yuImg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/g8Sm4_yuImg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/npX0_vBZtCI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/npX0_vBZtCI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

