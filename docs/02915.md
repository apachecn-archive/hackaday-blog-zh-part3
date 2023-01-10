# 并行压缩机用于喷砂，而不会破坏您的网格

> 原文：<https://hackaday.com/2016/07/12/parallel-compressors-for-sandblasting/>

[Hannah]正在修复一个 1962 年的大众 Bug。我们的目标是让这辆车及时上路，参加她的驾照考试。这可不是件容易的事，因为车身下部的 3 英寸已经生锈了，而且发动机也…失踪了。基本上，汽车需要一个框架关闭修复。这意味着[汉娜]将有很多金属车身需要清理。最简单的方法之一就是喷砂。

大规模喷砂与大多数气动操作略有不同。喷砂只需要适度的气压，但是需要高气流。喷砂需要 25 立方英尺每分钟(SCFM)80 磅/平方英寸的压力。大多数压缩机可以很容易地提供这一压力，但 25 SCFM 要求相当多。她可以买一台昂贵的三相机组，或者租一台柴油螺杆式压缩机。然而，[【汉娜】决定并联 4 台压缩机](https://www.youtube.com/watch?v=YGYgQO5TFto)给她需要的流量。

并联连接空气输出很容易。问题在于电力。每台压缩机运行时的额定电流为 9 安培。他们在启动时画得更多。压缩机必须连接到单独的 15 安培电路，以避免保险丝熔断。他们还需要按顺序启动，这样他们就不会在启动时拉下整个房子的空调。

Hannah 可以为此使用任何类型的延迟，但她选择了 Arduino。Arduino 的壁灯连接到主压缩机。打开主机会给 Arduino 通电，Arduino 会立即开始 2 秒钟的延迟。当延迟超时时，Arduino 会启动第二台压缩机。在几个延迟循环之后，所有 4 个压缩机一起运行。

Arduino 的 GPIO 引脚不能处理 9 安培的交流负载，所以[Hannah]将它们连接到 TIP120 晶体管。TIP120s 驱动低功率继电器，进而驱动高电流空调继电器。该系统工作得相当好，正如在休息下面的视频中可以看到的那样。

如果你对空气压缩机项目感兴趣，[看看这个由旧冰箱压缩机制成的装置](http://hackaday.com/2015/07/01/diy-air-compressor-made-from-refrigerator-and-fire-extinguisher/)。有关 TIP120 的更多背景信息，[请查看这篇关于这些有用晶体管的文章](http://hackaday.com/2015/08/17/you-can-have-my-tips-when-you-pry-them-from-my-cold-dead-hands/)。

 [https://www.youtube.com/embed/YGYgQO5TFto?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/YGYgQO5TFto?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

