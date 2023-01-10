# 虚拟啤酒乒乓机器人手臂

> 原文：<https://hackaday.com/2017/12/15/a-robot-arm-for-virtual-beer-pong/>

让工科学生来重新定义派对吧。[Hyun]、[Justin]和[Daniel]已经在他们的最终项目中完成了这一点，他们建造了一个虚拟控制的机器人手臂来玩啤酒乒乓。

这种构造有两个主要部分:用户佩戴的袖子和机器人手臂本身。该袖子在肘部和手腕处具有 IMU，以及计算它们各自角度的 PIC32。套筒将角度数据发送到第二个 PIC32，在 pic 32 中，角度数据被转换成 PWM 信号并发送到机械臂。

有一个压力传感器有线袖侧，戴在食指和拇指之间，作为一个释放机制。你实际上不需要把你的前臂向前扔来让机器人投球，但是如果你想的话，你可以这样做。手臂本身由三个微型伺服系统组成，安装时保持稳定。勺子是一种妥协。他们尝试了一段时间来模仿手指，但没有足够的时间来实现抓取和释放。

最初，该团队希望在袖子和手臂之间进行无线通信。他们让它与一对 XBees 一起工作，但发现 RF 只在短时间内有效。通过 UART 进行通信要流畅得多，你可以在下面的视频中看到这一点。

你不一定要有一个机械商店，甚至不一定要有一台 3d 打印机来制造一个机器人手臂。这是另一个由废木头制成的机器人，它的唯一目的是泡茶叶袋。

 [https://www.youtube.com/embed/LB6-ghAbCxQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/LB6-ghAbCxQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

