# 这个微小的马达内置在印刷电路板上

> 原文：<https://hackaday.com/2018/01/24/this-tiny-motor-is-built-into-a-pcb/>

在 PCB 上安装电机不是什么新鲜事，对吧？但是把 PCB 本身做成电机的一部分怎么样？这就是[Carl Bugeja]在 PCB 项目中用他的[无刷 DC 电机所做的，我们认为这很酷。](https://hackaday.io/project/39494-pcb-motor)

关于[Carl]的 Hackaday.io 页面的细节现在还不太清楚，但是我们已经和他联系过了，他给了我们一些信息。PCB 包含 BLDC 的定子，并作为转子轴承的机械支撑。PCB 上蚀刻有六个螺旋线圈，每个线圈约 40 圈。线圈围绕轴分布；它们以星形结构连接，驱动一个 3D 打印的转子，转子上压有四块磁铁。你可以在下面的视频中看到一个简短的测试；由于只有一个轴承，它似乎有一点轴向抖动，但是可以用一个帽板支撑上轴承来解决。

我们在这个设计中看到了很大的潜力。[Carl]提到线圈中缺少铁芯限制了其在低扭矩应用中的应用，但似乎可以在线圈中心钻孔并压入铁氧体嵌条。将 SMD 霍尔传感器添加到电路板上进行反馈也是可行的——事实上，将整个 ESC 和电机集成在一个 PCB 上也是可行的。[Carl]承诺将保持项目页面的更新，我们期待着更多的更新。

对于打印电机的更传统的方法，看看这个巨大的 3D 打印 BLDC。

 [https://www.youtube.com/embed/7pxUgC1YTQs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/7pxUgC1YTQs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

