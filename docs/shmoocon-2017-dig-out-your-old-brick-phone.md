# Shmoocon 2017:翻出你的旧砖头手机

> 原文：<https://hackaday.com/2017/01/16/shmoocon-2017-dig-out-your-old-brick-phone/>

90 年代是便携式通信设备的美好时代。手机有质量，真正的按钮，厚厚的电池——所有你想在明年的旗舰手机中看到的东西。不幸的是，扎克·莫里斯的手机在过去十年里一直无法找到一个塔，但这并不意味着这些手机已经死了。本周末在 Shmoocon 上，[Brandon Creighton]让这些手机起死回生。摩托罗拉·戴纳塔克又复活了。

[Brandon]有建立特设手机网络的历史。几年前，他是 Ninja Tel 的成员，该组织在 DEF CON 上建立了自己的手机网络。那是一个 GSM 网络，而 brickphones 要酷得多，所以在过去的几个月里，他将目光放在了构建 1G 网络上。[所有代码都在 GitHub](https://github.com/unsynchronized/gr-amps) 上，建一个 1G 的塔对硬件要求相当轻；你可以花大约 400 美元来铺设自己的 1G 网络。

构建 1G 网络的第一步，正确地称为 [AMPS 网络](https://en.wikipedia.org/wiki/Advanced_Mobile_Phone_System)，就是阅读文档。整个规范只有 136 页，简单到足以让一个人晕头转向，而且“呼叫”的概念实际上并不存在。AMPS 看起来更像一个中继系统，语音频道只是调频。所有这些信息都被翻译成 GNU 无线电块，Brandon 可以打电话给一部旧的摩托罗拉翻盖手机。

就硬件而言，与现代 SDR 硬件的功能相比，AMPS 是相当轻量级的。现场演示设置使用了一个 [Ettus 研究 USRP N210](https://www.ettus.com/product/details/UN210-KIT) ，但这是矫枉过正。这些手机以最小的带宽工作在 824-849 MHz 左右，因此基站可以很容易地由一个 HackRF 和一个 RTL-SDR 加密狗组装而成。

是的，手机是旧的，但有一个伟大的奖金关于放大器。在美国，没有人真正使用这些频率了。这并不是说在美国建造自己的未经许可的 1G 塔是合法的，但是如果没有人举报你，*你可能会逃脱惩罚*。