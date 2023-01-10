# 烦躁微调变得有用的 MIDI 控制器

> 原文：<https://hackaday.com/2017/09/16/fidget-spinner-gets-useful-as-midi-controller/>

坐立不安纺纱不仅是一种时尚，但几乎没有用。听起来像是黑客的工作，让玩具有一些实际用途。[D777k]接受了挑战，用一个普通的旋转器创造了一个 MIDI 控制器[。你可以在下面看到结果的视频。](http://www.instructables.com/id/Fidget-Spinner-MIDI-Controller/)

该设备使用浅蓝色 Bean 控制器和车库乐队作为 MIDI 软件。诚然，它可能不是超级有用的，但它总比只是一个普通的老式纺纱机要好。[D777k]称之为“旋转发声的苦行僧！

驱动这个东西的 Arduino 代码非常简单。它读取三个加速度轴，并使用它来驱动 MIDI 软件。当加速度超过阈值时，软件基于加速度的和与差创建新的音符。

浅蓝色 Bean [并不是什么新东西](https://hackaday.com/2015/08/05/lightblue-bean-adds-battery-connectors-price/)，但它非常适合这种服务。当然，把玩具做成 MIDI 控制器[也不是 T3 的原创想法。但这确实很有趣。](https://hackaday.com/2017/06/30/how-to-midi-interface-your-toys/)

 [https://www.youtube.com/embed/UsUsXSsQjjk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/UsUsXSsQjjk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

