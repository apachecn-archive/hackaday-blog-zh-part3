# 用于可穿戴设备的电容式和电阻式触摸传感器

> 原文：<https://hackaday.com/2018/03/17/capacitive-and-resistive-touch-sensors-for-wearables/>

当你考虑电子可穿戴设备的开关解决方案时，你的选择是有限的。通过导电织物和线的巧妙应用，您可以拼凑出一个简单的开关，但大量的开关解决方案远不止这些。[这个不一样](https://zpatch.github.io/)。哥本哈根大学以人为中心的计算部门的[Paul Strohmeier]、[Jarrod Knibbe]、[Sebastian Boring]和[Kasper hornk]的 zpatric 提供了 eTextiles 容性和阻性输入。这是一个力传感器，一个压力传感器，和一个开关，都是完全由织物制成的。

这种织物触摸传感器的设计基于 Eeonyx 制造的无纺电阻织物。这种织物受压时具有压阻性。这种材料夹在两层镀银聚酰胺织物之间，然后连接到微控制器的模拟输入端。在这一切之上是一个聚酯网，所有的东西都用熨板固定在一起。

用微控制器读取该传感器非常类似于由铜和 FR4 制成的电容式触摸传感器。[所有的代码都可以在一个 repo](https://github.com/zPatch/zPatch.github.io/blob/master/ArduinoCode/fabricSensor/fabricSensor.ino) 中找到，所有复制这个作品的材料都可以在团队提供的各个链接中找到。最后一点——再现性——对于一部学术著作来说非常重要。团队不仅设法想出了一些有趣的东西，他们实际上提供了足够的文档来重现他们的构建。

在下面的视频中，你可以看到这个传感器如何用来感应手的悬停、轻触、用力按压或两者之间的任何事情。每个传感器只需要两个模拟引脚，这使得电子织物的布线和布局相对容易集成到服装中。这是一个很棒的构建，我们迫不及待地想看到社区接受这些非常酷的传感器。

 [https://www.youtube.com/embed/88QgGQLsvpo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/88QgGQLsvpo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

