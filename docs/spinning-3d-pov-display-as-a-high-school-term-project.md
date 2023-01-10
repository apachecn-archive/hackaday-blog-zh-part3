# 旋转 3D 视点显示:高中学期项目

> 原文：<https://hackaday.com/2016/11/16/spinning-3d-pov-display-as-a-high-school-term-project/>

如果你是科幻剧的粉丝，你会习惯立体 3D 显示器，因为在未来某个遥远的时刻，它会变得非常棒。自从虚拟 3D[莱娅公主]在[R2D2]不太出名的*星球大战*影迷面前放映以来，已经过去了大约四十年，而在现实世界中，这仍然是一项还有一段路要走的技术。我们已经看到了发光二极管立方体、旋转阵列和投射到旋转圆盘上的激光，但是还没有什么能让我们感到*的惊喜！*标志着技术已经真正到来。

我们开始看到这些显示器从高端研究实验室转移到黑客和制造商的领域，我们为你准备的这个项目就是一个很好的例子。[Balduin Dettling]使用安装在转子上的多根可寻址 LED 棒创造了一个旋转的 LED 显示器[，并由一个 Teensy 3.1 驱动。让这一切更加引人注目的是，他是德国一所中学的学生(想想英国的文法学校或美国的预科学校)。](https://github.com/mbjd/3DPOV)

他的显示器上有 480 个发光二极管，他通过 TLC5927 移位寄存器对它们进行寻址。同步由霍尔效应传感器和磁铁提供，以检测每次旋转的开始，Teensy 根据该时间调整其像素速率。他在 GitHub 资源库中提供了极其全面的文档，包括代码和构造细节，包括值得深入研究的英文白皮书。他还上传了我们给你的两段视频。

你高中的时候在做什么？它涉及电路设计、机械制造、固件和文档吗？对于这样一个年轻的黑客来说，这是一套令人印象深刻的技能，也是我们希望看到的对工程职业感兴趣的人可以获得的教育类型。

 [https://www.youtube.com/embed/-gFsKhf5J-I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/-gFsKhf5J-I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/bCETWNgBxbI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/bCETWNgBxbI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



我们之前已经给你们展示过一两个立体 3D 展示，如果能想到这个展示会鼓励更多的展示，那就太好了。为了激起你的兴趣，这里有一个带有[旋转螺旋](http://hackaday.com/2015/10/29/3d-printed-helix-displays-graphics-in-3d/)，另一个类似于这里的[使用 LED 棒](http://hackaday.com/2014/04/21/volumen-the-most-advanced-persistence-of-vision-display-yet/)。