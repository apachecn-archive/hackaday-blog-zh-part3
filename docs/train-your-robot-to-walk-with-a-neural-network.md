# 训练你的机器人用神经网络行走

> 原文：<https://hackaday.com/2016/12/11/train-your-robot-to-walk-with-a-neural-network/>

[巴斯蒂]正在研究人工神经网络(ann ),并认为许多“你好世界”类型的程序不够生动，不足以向他人灌输他对网络的热爱。因此，他通过应用一个相当简单的人工神经网络来教一个四条腿的机器人走路，使它变得更有活力。

虽然我们认为世界各地的邮政系统多年来一直在根据类似的算法对邮件进行机器分拣，这很棒，但看着蠕动的四个伺服系统达成前进的共识更令人鼓舞。干得好！查看嵌入在下方的[视频。](https://www.youtube.com/watch?v=fHCm0gQRzC4)

网络的细节很简单。为了减少输出状态的数量，每个伺服只能假设三个位置。输入包括当前和先前的腿位置。它的前面有一个距离传感器，所以它可以知道它什么时候取得了进展，就是这样。剩下的就是让它摆动 15 分钟，偶尔调整一下位置。

这一切都是通过将 [Fast ANN 库](http://leenissen.dk/fann/wp/)移植到 Cortex M4 微控制器而成为可能的，这又要求【巴斯蒂】将一个小型只读文件系统移植到芯片上。通读他的博客了解详情，或者直接跳到[的代码](https://github.com/Counterfeiter/Q-LearningRobot)，如果那更符合你的风格。

我们会说，如果你对学习人工神经网络感兴趣，像这样的实践应用是一个了不起的动力。如果你想在开始之前温习一下基础知识，可以看看[Al]关于这个主题的两部分系列([一个](https://hackaday.com/2016/11/02/machine-learning-foundations/)和[两个](https://hackaday.com/2016/11/08/perceptrons-in-c/))。与此同时，我们给你留下了挥舞拉链乐高积木的视频。

 [https://www.youtube.com/embed/fHCm0gQRzC4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/fHCm0gQRzC4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

