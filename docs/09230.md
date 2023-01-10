# 用于 ESP32 的快速 LED 矩阵图形

> 原文：<https://hackaday.com/2018/04/21/fast-led-matrix-graphics-for-the-esp32/>

你们中的许多人都曾尝试过从微控制器项目中驱动显示器，对于大多数人来说，这意味着非常简单的状态信息，你会使用标准库，而不太关心它们的性能。然而，如果你们中的任何人需要快速更新图形，如视频或游戏内容，你可能会发现简单的软件解决方案不够快。如果你是一个 ESP32 用户，那么，[Louis Beaudoin]可能会给你带来一些好消息，因为[他已经将 SmartMatrix 库移植到那个平台上](https://hackaday.io/project/148066-smartmatrix-library-esp32-port)。我们已经看过了他的演示，在休息时间下面的视频中可以看到的结果确实令人印象深刻。

如果你想知道 [SmartMatrix 库](http://docs.pixelmatix.com/SmartMatrix/)是什么，这是一个面向青少年的 LED 矩阵库。[Louis]的 port[可以在 GitHub](https://github.com/pixelmatix/SmartMatrix/tree/teensylc)上找到，正如他在我们的剑桥聚会上喝啤酒时向我们解释的那样，它充分利用了 ESP32 的 DMA 功能。让微控制器以任何速度与显示器对话显然是目前的一个热门话题，[Radomir dopieraski]几周前在我们的 Dublin Unconference 上的[演讲](https://hackaday.com/2018/04/11/dublin-unconference-roundup-the-most-interesting-tech-topics-right-now/)谈到了同样的话题。

我们不得不承认 Hackaday 对 LED 面板情有独钟，鉴于 ESP32 的强大功能，我们期待着使用这个库来编写预期的项目。

 [https://www.youtube.com/embed/mprokFj-WjY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/mprokFj-WjY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

