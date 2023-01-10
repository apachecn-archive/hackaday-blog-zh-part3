# 控制这款智能手表全在手腕上

> 原文：<https://hackaday.com/2016/11/26/controlling-this-smartwatch-is-all-in-the-wrist/>

智能手表非常棒。理论上，你永远不会错过通知或电话。此外，它们可以进行各种生物计量跟踪，因为它们被绑在你身体的一个脉搏点上。但是也有不利的一面。其中一个主要问题是，你最终需要两只手来做一些在手机上单手就能轻松完成的事情。现在，你可以像我在冬天戴手套时那样用鼻尖，但那对你的眼睛不好。看来智能手表输入的未来不在可用的附属物，而在手势检测。

进入 [WristWhirl](http://www.dartmouth.edu/press-releases/wristwhirl-joystick-101416.html) ，达特茅斯和曼尼托巴大学学生【龚俊】、【兴·】、【普朗·】的大脑产物。他们已经建立了一个智能手表原型，使用红外接近传感器检测的连续手腕运动来控制流行的现成应用程序。十二对连接到 Arduino Due 的非常便宜的红外传感器可以检测佩戴者做出的八个简单手势中的任何一个，以完成诸如打开日历、控制音乐播放器、平移和缩放地图以及玩俄罗斯方块和水果忍者等游戏的任务。为了节省电池，压电感应用户拇指和食指之间的挤压，并使用这种输入来决定何时开始和停止手势检测。

根据[他们的论文](http://xingdongyang.net/papers/Wristwhirl.pdf) (PDF 警告)，手势检测准确率 93.8%。为了获得这些数据，研究小组让他们的测试对象在不同的条件下表演八种手势中的每一种，例如行走与站立，或者手腕处于观看手表的位置或者垂在身体两侧。为什么不示意休息时间过去观看演示呢？

如果你坚持用手势玩俄罗斯方块，还有其他方法。

 [https://www.youtube.com/embed/JTPzeZGiI8w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/JTPzeZGiI8w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[通过[嵌入式实验室](http://embedded-lab.com/blog/using-wrist-joystick-controlling-smartwatch/)