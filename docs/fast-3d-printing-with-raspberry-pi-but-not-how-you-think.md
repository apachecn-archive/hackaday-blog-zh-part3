# 使用 Raspberry Pi 实现快速 3D 打印——但不是你想的那样

> 原文：<https://hackaday.com/2017/12/26/fast-3d-printing-with-raspberry-pi-but-not-how-you-think/>

虽然我们倾向于认为 3D 打印机是高科技玩具，但大多数 3D 打印机在大脑部门并不是特别强大。有一些例外，但大多数 3D 打印机都运行在 8 位 Arduino 或一些具有大量 I/O 的 Arduino 变体上。有一些 32 位的主板，但如果你随机选择一台 3D 打印机，它的大脑将是一个 8 位 AVR，运行类似 Marlin 或 Repetier 的东西。看到 Raspberry Pi 连接到打印机并不罕见，但一般来说，它是一个网络接口，用于向运行步进电机的 8 位控制器发送 g 代码。在相对强大的 Raspberry Pi 中做诸如解析 g 代码、绘制曲线和设置加速度之类的事情，而将 8 位 AVR 仅用于命令电机和加热器，这是否更有意义？[KevinOConnor]是这样认为的，他写了 [Klipper](https://github.com/KevinOConnor/klipper) 来证明这一点。

Klipper 主要是用 Python 编写的，它完成了传统 3D 打印固件的大部分功能。它通过提供何时做什么任务的时间表来与板载微处理器通信。微处理器然后处理时间和事情，如轴和挤出机的运动控制。Klipper 可以轻松控制多个微处理器，并使它们保持同步，例如，您可以为您的挤出机和每个步进机配备一个处理器。您可以将 Klipper 与笛卡尔机、delta 或核心 XY 型打印机配合使用。

主机甚至不一定是树莓派。BeagleBone 可以工作——至少在理论上——任何 Linux 计算机都可以。你在微控制器上编写了一小段固件，它向主计算机传达一个轻量级协议。至于用户界面，那很简单。主机可以和 Octoprint 对话，你可以在运行 Klipper 的同一个 Raspberry Pi 上运行它。

微控制器固件只有少量的命令。其中大部分都与给定时间内要做的事情有关:操作步进电机或设置 PWM 输出。因为它很简单，你可以有一个小的 CPU，你可能会得到更快的速度。当然，这是假设你的硬件可以处理更快的速度。

## 特征

Klipper 吹嘘了几个“引人注目的特征”:

每个步进器事件以 25 微秒或更高的精度进行调度。该软件不使用运动学估计(如 Bresenham 算法)。它根据加速度物理学和机器运动学物理学计算精确的步进时间。更精确的步进器移动意味着更安静、更稳定的打印机操作。

由于微控制器固件非常简单，所以只需更改主机上的一个文件，就可以轻松地在 Klipper 中重新配置。固件很简单，用 C 语言编写，因此它可以支持许多微处理器，包括 3D 打印机中常见的 8 位和 32 位 CPU。

Klipper 能够实现精确的高步进率。较老的 AVR 显然可以达到每秒 175，000 步以上的速率，并且高达每秒 500，000 步的速率是可能的。步进速率越高，打印速度越快。

在高打印速度下，渗色可能是一个问题。Klipper 为挤出机实现了“压力提升”算法。当适当调整，压力进步减少挤出机渗出，可能允许更快的印刷。你可以在下面看到一个视频，布拉德利·穆勒使用 Klipper 以 100 毫米/秒的速度打印。

 [https://www.youtube.com/embed/-saoFQll2NM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/-saoFQll2NM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



如果这还不够快，请从[lenne 0815]以 150 mm/s 的速度查看这个立方体(等待第一层完成):

 [https://www.youtube.com/embed/X2bYn47-snU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/X2bYn47-snU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



还有一种新颖的“步进相位终点停止”算法，可以提高典型终点停止开关的精度。这对于 Z 终点挡板尤其重要，因为这可以获得更精确的第一层高度，并提高印刷质量和附着力。

## 调谐

其中一些特性确实需要调整。例如，压力提前算法需要特定于机器的常数。下面是来自[文档的一些描述软件运动学](https://github.com/KevinOConnor/klipper/blob/master/docs/Kinematics.md)的文本:

> “压力推进”系统试图通过使用不同的挤出机模型来解决这一问题。它没有天真地认为每立方毫米喂入挤出机的长丝都会导致该立方毫米立即离开挤出机，而是使用了一个基于压力的模型。当细丝被推入挤出机时，压力增加(如[胡克定律](https://en.wikipedia.org/wiki/Hooke%27s_law))，挤出所需的压力由通过喷嘴孔的流速决定(如[泊肃叶定律](https://en.wikipedia.org/wiki/Hagen%E2%80%93Poiseuille_equation))。关键思想是细丝、压力和流速之间的关系可以使用线性系数来建模。

您可以通过打印一个测试方块并找到给出一个好看的角的最小数字来实验性地找到该值。例如，下面左边是一个失谐的角，右边是一个正确的角。

 [![Mistuned corner](img/65e484e43684165d9d524fafc9ee6d5d.png "corner-blob")](https://hackaday.com/2017/12/26/fast-3d-printing-with-raspberry-pi-but-not-how-you-think/corner-blob/) Mistuned corner [![Correctly tuned](img/e621e2aef9ba2bee6e7f19442b24300e.png "corner-good")](https://hackaday.com/2017/12/26/fast-3d-printing-with-raspberry-pi-but-not-how-you-think/corner-good/) Correctly tuned

终点挡板功能利用步进电机驱动器的相位。例如，16 微步的步进驱动器有 64 个不同的相位。你可以回到步进电机的分辨率，而不是回到一步的分辨率。

## 进入壁垒

是什么阻止你尝试克利珀？你可能有一个树莓皮挂在附近。Klipper 的固件可能适用于您当前打印机的 CPU(只要确保您知道如何在上面闪存代码，并有一份您当前固件的副本)。

我们不禁想到，如果你能在 Linux 笔记本电脑上实现这一点，你就可以为你的打印机配备一个超级控制面板。当然，无论如何你都可以这样做，但是如果你用笔记本电脑直接连接 Octoprint，你会把更多的计算能力留在桌面上。

从黑客的角度来看，能够使用 Python 在 ssh 上修改 3D 打印算法，而不必刷新微控制器，这应该开辟了许多实验的可能性。如果你有一个有趣的叉子，一定要给我们一个提示，我们会在这里涵盖它。