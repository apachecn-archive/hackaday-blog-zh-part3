# 使用 DLP 3D 打印机进行亚像素打印

> 原文：<https://hackaday.com/2016/07/26/get-subpixel-printing-with-a-dlp-3d-printer/>

DLP 3D 打印机的工作原理是使用数字光处理投影仪将光照射到光敏聚合物的大桶中，固化一薄层粘性物质，直到形成固体部分。通常，印刷品的分辨率由投影仪的分辨率和聚合物本身的成分决定。但是，Autodesk 为他们的 Ember DLP 3D 打印机发布的一项技术可以让你基本上[消除你的打印](https://www.youtube.com/watch?v=5qTAmPrHLow)的锯齿，进一步提高有效分辨率。

 [https://www.youtube.com/embed/5qTAmPrHLow?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/5qTAmPrHLow?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



该技术通过对每层投影的图像使用灰度抗锯齿来工作。灰色光线越暗，聚合物固化的时间越长。因此，如果用在关键点，它可以沿边缘平滑打印。这类似于 TrueType 字体和其他图形显示技术如何在视觉上平滑字体和图形的边缘，以给出更平滑线条的印象。

现在，Autodesk Ember [是开源的，这对社区](https://ember.autodesk.com/overview#open_source)来说非常好。~~是一台专有的 3D 打印机——这是我们这里不太喜欢的东西~~。但是，没有任何理由这项技术不能用于其他 DLP 3D 打印机。即使是你自己建造的。虽然这个调整很简单，但是可以很有把握地认为它很快会成为一个非常标准的输出选项。

[via [reddit](https://www.reddit.com/r/3Dprinting/comments/4u3dd9/trick_for_getting_subpixel_resolution_on_autodesk/)