# 黑客日链接:2018 年 5 月 20 日

> 原文：<https://hackaday.com/2018/05/20/hackaday-links-may-20-2018/>

来自好莱坞的一项似乎永远不会成为现实的更有趣的技术是位置追踪器。还记得*外星人*里那个在储物柜里发现猫的‘运动追踪器’吗？对，就像那样。报告目标的方向和距离的东西，有点像来自*捉鬼敢死队*的 PKE 米。我认为在《T4 掠夺者》中也有类似的东西。在 Indiegogo 上，有一个设备可以跟踪其他设备。它被称为 Lynq，是一个小型的手持设备，可以告诉你其他配对设备的距离和方位。把它们发给你的朋友，你就能在科切拉找到彼此。虽然设备和用例很有趣，但我们想知道它到底是如何工作的。我们的最佳猜测是，每个设备内部都有一个 GPS 模块，并通过 900MHz 频段与其他配对的设备进行通信。每台 80 美元有点贵(虽然你至少需要两台才有用)，但这是一个非常有趣的项目。

正如你所猜测的，SDRPlay SDR1 和 SDR2 是软件定义的无线电接收机，零售价为 2-300 美元。问题:这些设备中有一些是从一个仓库中被偷的，现在正被运往易贝。解决方案:SDRPlay 已决定[通过序列号](https://phasenoise.livejournal.com/5612.html)禁用特定接收器。一家制造商决定将被盗或侵犯知识产权的产品制成砖块，这有点像 FTDIgate。这是*的一个*解决方案，但我不想加入 SDRPlay 的客户服务团队。

几年前，[【Oscar】创造了 PiDP-8/I](https://hackaday.io/project/4434-pidp-8i) ，这是一个计算机套件，它将古老的 PDP-8/I 小型化成一个桌面外形，配有闪光灯和 clicky 开关。这是在 Raspberry Pi 上运行的 PDP-8 的完整模拟，如果你把 PiDP-8/I 带回 1975 年，你确实可以把它连接到其他计算机上。但是 PDP-8/I 并不是有史以来最漂亮的小型机。这一荣誉属于 PDP-11/70，它是一台包裹在注射成型塑料和紫色拨动开关中的机器怪兽。现在，经过多年的努力，[奥斯卡]已经将这台机器小型化了。[PiDP-11/70 是 PDP-11/70](https://hackaday.io/project/8069-pidp-11) 的微型翻拍版，运行树莓 Pi，是你在迷你框架中想要的一切。价格大约在 250 美元左右——很贵，但是你有没有试过*在易贝找到*一个 PDP-11 前面板？

Nvidia TX2 是一台信用卡大小的电脑，配有强大的 ARM 处理器*和 GPU*。TX2 是一个为“AI at the edge”或类似产品设计的模块，这意味着你可以获取一个经过训练的数据集，将其加载到 SD 卡上，TX2 将在没有互联网连接的情况下完成所有复杂的图像处理和 OpenCV。TX2 的明显应用是类似“人工智能相机”的东西，[现在这终于是一个产品](https://groupgets.com/campaigns/429-dnncam-ai-camera)。DNNCam 是一个 4k、60FPS 的摄像机，连接到 TX2，并装入 IP67 防护等级的外壳中。如果您正在考虑构建类似连接到 GPU 的安全摄像头的东西，这是一个一体化的解决方案。是的，它很贵，但是 TX2 模块并不便宜。