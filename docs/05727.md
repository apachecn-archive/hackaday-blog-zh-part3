# 如何对芯片进行逆向工程

> 原文：<https://hackaday.com/2017/05/02/how-to-reverse-engineer-a-chip/>

你有没有想过如何观察芯片并绘制出它的原理图？[Robert Baruch]想在一个新的视频中向你展示他是如何做到的(见下文)。该视频假设您知道如何曝光骰子，因为他之前制作过相关视频。

这段视频重点介绍了如何使用他的比格犬骨驱动的显微镜载物台，从较小的镜头中获得高分辨率的显微照片。3D 打印的样品支架可以防止零件四处移动。幸运的是，有软件可以将图像拼接在一起。一旦他有了芯片照片，他将蚀刻掉金属以去除钝化层、金属层和金属下的二氧化硅，并拍摄另一组照片。

[Robert]将图像加载到 Inkscape 中，以便他可以跟踪设备的各种组件并添加标签。然后他用 KiCAD 制作原理图。最终结果是项目 54/74 wiki 上的一个[条目。我们之前提到的项目旨在记录这一具有历史意义的 IC 家族。](https://hackaday.com/2017/04/04/project-5474-maps-out-logic-ics/)

如果你想重复他的努力，要注意你需要一些相当讨厌的化学物质，所以要小心。真正的实验室用氢氟酸蚀刻玻璃，特别恶心。[Robert]使用 Armour Etch，速度较慢，但更安全，也更容易获得和储存。

视频主题 74LS01 只有 8 个晶体管。想象一下，试图用大约 3500 个更小的晶体管来做一个简单的 CPU，比如 8008 T1。我们推荐咖啡和耐心。

 [https://www.youtube.com/embed/r8Vq5NV4Ens?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=6&wmode=transparent](https://www.youtube.com/embed/r8Vq5NV4Ens?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=6&wmode=transparent)

