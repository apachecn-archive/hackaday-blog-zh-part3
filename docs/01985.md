# 使用一个摄像头进行惊人快速的 3D 跟踪

> 原文：<https://hackaday.com/2016/04/02/insanely-quick-3d-tracking-with-1-camera/>

让我们面对它:三维里程计可能是一个计算量很大的问题，通常需要昂贵的 3D 相机和优化的算法，这可能很难让我们理解。然而，研究人员每年都在继续推进视觉里程计的界限。过去的一年也不例外，因为[Christian]、[Matia]和[Davide]已经用一种可以在 3D 中实时跟踪自身的算法打破了速度的天平。

在视频中(休息后)，地标稀疏，要跟踪的运动无情地呈锯齿状，但 SVO，或**S**EMI-Fast**V**isual**O**dometry[[PDF warning](http://rpg.ifi.uzh.ch/docs/ICRA14_Forster.pdf)]，利用“高频纹理”作为参考，以惊人的一致性保持跟踪精度。其他一些实现需要两个相机或一个深度相机变体，但不需要 SVO。它使用单个相机，具有每秒 55 到 300 帧的高帧率。最棒的是，苏黎世大学的三人组将他们的代码库开源，并作为 [ROS](http://hackaday.com/2014/01/29/the-robot-operating-system-ros-101/) 的软件包提供。

 [https://www.youtube.com/embed/2YnIMfw6bJY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/2YnIMfw6bJY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

