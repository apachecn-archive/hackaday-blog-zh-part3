# 我想要的圣诞礼物就是一个四因子生物识别锁盒

> 原文：<https://hackaday.com/2016/12/13/all-i-want-for-christmas-is-a-4-factor-biometric-lock-box/>

这是一年中最美好的时光！不，我们不是在谈论假日季节，尽管那肯定有它的优点。我们的意思是，现在是[Bruce Land]的 ECE4760 课程的最终项目时间。考虑到奉献精神和他们的母亲，[Adarsh]、[Timon]和[Cameron]制作了一个具有四因素认证的可编程锁箱。这比拉斯维加斯普通的酒店房间保险箱安全三倍，而且还配有显示器。

要进入这个盒子，首先要在数字键盘上输入一个四位数的密码。如果不正确，显示屏会显示出来。输入正确的代码，系统将等待 4 秒钟进行下一步，这涉及到三个电位计。这些被调整到正确的值，偏差为+/-30°。再等四秒钟后，它就接通了基于压电的爆震检测器，该检测器监听正确的模式。最后，指纹扫描仪确保任何想要进入这个盒子的人最好提前计划好。

这个项目基于 Microchip 基于 PIC32 的 Microstick II，该项目 Land 教授]将于 2015 年开始教学。它还使用 Arduino Uno 来处理指纹扫描仪。该团队在这个项目中考虑了适销性，在休息后的视频中，他们浏览了工厂设置和用户定制。

我们见过很多保护保险箱的方法。一个激光切割组合保险箱或[一个配有 NFC 戒指的盒子](https://hackaday.com/2014/08/10/nfc-ring-lock-box/)怎么样？

 [https://www.youtube.com/embed/VDu1fERQY6U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/VDu1fERQY6U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

