# 3D 打印螺旋以 3D 方式显示图形

> 原文：<https://hackaday.com/2015/10/29/3d-printed-helix-displays-graphics-in-3d/>

看起来,[Michel David]和他在 volumetric 的团队真的提升了他们的游戏:制作 3D 立体视频显示。

我们已经介绍了相同技术的早期版本，但是最好的技术解释仍然可以在他们的旧网站上找到。但这是一个足够简单的想法，我们预计所有的困难是在使细节工作。但是如果你看看他们的最新视频(就在跳转下面)，我们认为你会同意他们已经解决了大部分问题。

 [https://www.youtube.com/embed/ihZ_mJ04U3c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ihZ_mJ04U3c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



最新版本使用标准的高射投影仪(“德语”中的“投影仪”)将图像投射到旋转的螺旋线上。通过与转子同步快速改变图像，您可以选择光束击中开瓶器的高度。旋转转子(在 Dremel 上！)足够快，剩下的就交给你的 POV 了。我们非常喜欢当前设置的简单性，结果不言自明。

计算出每个光点应该投射的确切位置和时间绝非易事，但如果你有一个非常精确的螺旋模型，这应该是可能的。这使得这成为大型 3D 打印机的完美借口——理想情况下，你可以在电脑上制作一个螺旋模型，然后打印出完全相同的形状。

我们希望看到更多关于新版本的细节，也许还有一些软件的链接。我们仍然有一个困扰的问题:他们如何在旋转的螺旋线和视频显示之间获得同步？我们看不到任何旋转传感器或反馈。是刚调好的吗？