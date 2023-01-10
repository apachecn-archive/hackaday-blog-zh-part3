# 机器人瞄准眼球，发射激光。OSHA 会喜欢这个的

> 原文：<https://hackaday.com/2017/04/18/robot-targets-eyeballs-fires-lasers-oshas-gonna-love-this-one/>

如果你想用激光进行黑客攻击，你会听到关于眼睛安全的问题。他们会说“小心点”。“不要用剩下的眼睛看激光”是一个你无法避免的笑话。你会听到“你的护目镜在哪里”，以及大约 1000 个其他警告。不要误解我们，激光/眼睛安全很重要。然而，持续的警告可能会有点过时——特别是当你使用“低功率”3a 级激光时——你知道，就是那种在黄色背景上用黑色大字写着“避免直接接触眼睛”的警告标签。

[迈克尔·里维斯]厌倦了，变得有点疯狂。他制造了一个机器人，专门向人的眼睛发射激光。不，不是医疗机器人。这个机器人生活在披萨盒里，由伺服系统、胶带和迈克尔的眼泪组成。它只是向人们的眼睛发射激光。不用说，请不要在家里尝试这个，或者根本不要尝试。

设计这样一个恶魔般的野兽实际上相当简单。软件是用 C#写的。帧是从一个旧的罗技网络摄像头捕获的，然后传递到 [Emgu CV](http://www.emgu.com/wiki/index.php/Main_Page) ，这是 OpenCV 的一个. NET 包装器。[迈克尔]运行一个简单的面部检测算法，并使用结果来瞄准激光。激光器安装在两个遥控式伺服系统上。Arduino 形成了伺服系统和个人电脑之间的粘合剂。

[迈克尔]有一个伟大的面无表情的交付，这一切使一个伟大的视频。把他想象成一个在 Electroboom 公司工作的年轻的 Medhi。但我们不能纵容这种行为。正确标记和描述的红色激光笔[从未被证明会导致眼睛损伤](https://www.scientificamerican.com/article/can-a-pocket-laser-damage/)。然而，如果激光不符合规格或反射的东西进一步聚焦光束，它肯定会损害视力。

我们希望[迈克尔]的视力保持完好，这样他就可以制作更多的视频——他很有趣，即使无视安全警告也不是。

 [https://www.youtube.com/embed/Q8zC3-ZQFJI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Q8zC3-ZQFJI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

