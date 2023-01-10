# 用微小的激光束找到你的路

> 原文：<https://hackaday.com/2017/12/31/find-your-way-with-tiny-laser-beams/>

在嵌入式微控制器课程的最后一个项目中，[Aaheli、Jun 和 Naomi]将他们的注意力转向了辅助技术，并为视力障碍者创造了一种电子旅行助手(ETA ),它使用触觉反馈来报告障碍物的存在。

我们在过去见过一些这种类型的设备，它们几乎总是使用超声波传感器来测量距离。这个埃塔就不是这样了；它使用六个 VL53L0X 飞行时间(ToF)传感器，安装在彼此略有不同的角度，这提供了一个广泛的传感地图。它能够在距离传感器一米的范围内探测到一米宽的物体。

该设备由两部分组成，寻路棒和反馈模块。六个 ToF 传感器被绑在手电筒主体的末端，并连接到主体内的 Arduino Mini。Mini 通过 UART 接收传感器数据，并将其发送到必备的 PIC32，pic 32 附在用户前臂的袖子上。PIC 将这些 UART 信号解码为 PWM，并点亮六个相应的振动圆盘电机，这些电机悬挂在袖子上，并在前臂上侧形成一个传感手镯。

我们喜欢用 ToF 而不是超声波来寻路。无论 ToF 是否更快，它的足迹都要小得多，因此对于谨慎的辅助可穿戴设备来说更实用。另外，你知道，激光。休息之后，您可以在演示视频中看到它的效果。

这个装置旨在增强传统的白色手杖，而不是取代它。[我们几年前看到的这个虚拟拐杖](https://hackaday.com/2014/04/12/a-virtual-cane-for-the-visually-impaired/)就是另一个故事了。

 [https://www.youtube.com/embed/SUwN-Rnrqak?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/SUwN-Rnrqak?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

