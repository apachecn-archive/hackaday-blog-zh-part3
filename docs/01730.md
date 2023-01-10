# 我的谜

> 原文：<https://hackaday.com/2016/03/09/mein-enigma/>

二战时期德国的恩尼格玛编码机是工程界的一个标志，不仅因为它的机械独创性，还因为布莱奇利公园的战时工作人员破译了它的信息。如果没有它，我们就不会有第一台可编程数字电子计算机——巨像，随后的技术发展可能会以更慢的速度走向我们今天认为理所当然的东西。

遗憾的是，对于英格玛迷来说，真正的机器现在已经很少了。我们的祖父母那一代人通过欧洲各地的混乱和轰炸看到了这一点。如果你想处理一个，你必须要么有一大笔钱，为博物馆工作，或者为 GCHQ 档案员工作。

这并没有阻止我们的社区构建 Enigma 副本，最近在 Hackaday 引起我们注意的一个副本显示了一些希望。[lpaseen]的[meinegma 是由 Arduino Nano 驱动的电子谜](https://hackaday.io/project/10051-meinenigma)，旋转编码器代表 Enigma 转子，多段字母数字显示器代表原件中的发光字母。它在软件上支持所有不同类型的转子，有一个物理插板和一个 USB 串行端口，通过它可以控制所有机器功能。目前的机器是一个完整的工作原型，计划是最终的机器将尽可能地与原型相似。

[项目中使用的所有代码都可以在 GitHub](https://github.com/lpaseen/myEnigma) 上找到，还有[【LPA seen】的 Arduino 库](https://github.com/lpaseen/ht16k33)，用于处理那些任务的 [Holtek HT16K33](http://www.holtek.com/english/docum/consumer/16K33.htm) 键盘/显示芯片。

这些年来，我们在 Hackaday 上展示了一些英格玛机器。一个是装在手表里的[，另一个是装在被](http://hackaday.com/2015/03/23/enigma-machine-wristwatch/)[黑掉的儿童玩具里的](http://hackaday.com/2011/02/15/wwiis-top-cryptography-comes-to-a-childs-toy/)，但是最接近【lpaseen】的是这个[相当吸引人的复制品](http://hackaday.com/2013/10/07/arduino-based-enigma-replica-is-fully-functional/)，也是由 Arduino 驱动的。同样值得一提的是，如果你去白金汉郡旅行，你可以参观[布莱奇利公园博物馆](http://www.bletchleypark.org.uk/)和邻近的[国家计算机博物馆](http://www.tnmoc.org/)，从源头了解这个谜和巨人的故事。