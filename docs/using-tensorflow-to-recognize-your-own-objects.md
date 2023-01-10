# 使用 TensorFlow 识别您自己的对象

> 原文：<https://hackaday.com/2018/05/23/using-tensorflow-to-recognize-your-own-objects/>

当需要添加一个对象识别器时，你需要做的就是从许多可用的对象识别器中进行选择，并针对你感兴趣的特定对象对其进行重新训练。为了帮助这一点，[Edje Electronics]已经整理了一个使用 TensorFlow 来重新训练谷歌的 Inception 对象识别器的分步指南。他这样做是为了 Windows 10，因为已经有很多关于 Linux 操作系统的文档了。

但是你不仅仅局限于《盗梦空间》。《盗梦空间》是为数不多的非常精确的软件之一，但它需要几秒钟来处理每一张图像，因此更适合快速的笔记本电脑或台式机。MobileNet 就是一个例子，它不太准确，但识别速度更快，因此更适合于树莓 Pi 或移动电话。

你需要几百张你的物品的图片。这些图片可以从网上搜集，比如谷歌的图片，或者你可以自己拍照。如果你使用后一种方法，一定要从不同的角度、旋转和不同的光线条件下拍摄。用各种其他的东西填充你的背景，甚至让一些东西部分遮挡你的物体。这听起来可能是一个漫长而乏味的任务，但它可以有效地完成。[Edje Electronics]正致力于识别扑克牌，所以他首先将扑克牌撒在他的客厅周围，添加一些杂物，然后四处走动，用他的手机拍照。一旦上传，一些易于使用的软件帮助他在大约一个小时内将它们全部贴上标签。请注意，他在 24 种不同的物体上进行训练，这是你在一副[扑克牌](https://en.wikipedia.org/wiki/Pinochle)中得到的不同牌的数量。

你需要安装大量的软件并进行一些配置，但他也会指导你完成这些工作。理想情况下，你会使用一台带有 GPU 的计算机，但这是可选的，区别在于 3 小时或 24 小时的培训。请务必观看下方的[视频，并遵循其 Github 页面上的步骤。Github 页面保持最新，但他的视频更全面地指导您使用该软件，例如如何使用图像标签程序。](https://www.youtube.com/watch?v=Rgpfk6eYxJA)

为什么他要在扑克牌上训练一个物体识别器？这只是让[成为 21 点游戏机器人](https://hackaday.io/project/27639-rainman-20-blackjack-robot)的又一步。之前[他已经使用 OpenCV](https://hackaday.com/2017/10/13/a-raspberry-pi-rain-man-in-the-making/) 完成了令人印象深刻的工作，尽管该算法只处理非重叠的卡片。然而，谷歌的 Inception 可以识别部分模糊的卡片。这是一个非常有趣的项目，我们将密切关注它。如果你对他有任何想法，请在下面的评论中留下。

 [https://www.youtube.com/embed/Rgpfk6eYxJA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Rgpfk6eYxJA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

