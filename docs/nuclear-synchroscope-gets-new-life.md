# 核同步示波器获得新生

> 原文：<https://hackaday.com/2018/05/18/nuclear-synchroscope-gets-new-life/>

同步示波器是一种有趣的发电厂仪器，它是二合一设备。如果发电机频率与电网频率不匹配，同步示波器指针的旋转方向指示频率(发电机速度)是否需要增加或降低。当它停止旋转时，指针角度指示发电机和电网之间的相位差。当他得到一台在核电站控制室里曾经风光过的旧同步示波器时，他决定用它作为一个长期悬而未决的计划的外壳，建造一个数码管项目。结果——一个 [Arduino 谢妮时钟和气象站](https://www.instructables.com/id/Arduino-Nixie-Clock-Weather-Station/)——是一个复古现代外观的仪器，可以指示时间、温度、压力和湿度，同步示波器指针现在可以指示大气压力。

他没有复制现有的设计，而是决定从头开始构建他的项目，一边学习新的技术和技巧，一边改进他的设计。[badjer1]是 Fortran 的老前辈，所以他投身于 Arduino 生态系统是值得称赞的。除了时髦的外壳，大多数电子设备都是由现成的模块组装而成的。同步示波器不够大，无法容纳电子设备，所以[badjer1]不得不将其分成两半，并在中间添加一个透明的丙烯酸盒来容纳所有电子设备。为了增加视觉效果，他在外壳内安装了几个发光二极管。除了机械装配之外，可能他最大的挑战是确保他在显示面板上得到正确的谢妮电子管的切口。一个错误的举动，他会以一块铝垃圾和一个失踪的面板结束。

作为 Arduino 的新手，为了自己和他人的利益，他小心翼翼地将自己的代码分成易于管理的小块，并在其中加入大量注释。电子和硬件装配也同样详细，如果有人想尝试复制他的建设。仍然有改进的空间，特别是传感器的安装，但现在，[badjer1]似乎对结果很满意。休息后请观看演示视频。

谢谢你的提示，[克里斯芒西]。

 [https://www.youtube.com/embed/9zIeVyw2Jqg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/9zIeVyw2Jqg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

