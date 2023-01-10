# 用原力打开这盏灯

> 原文：<https://hackaday.com/2017/05/27/use-the-force-to-turn-on-this-lamp/>

全息记录仪是全息数据存储设备，在*星球大战*宇宙中被绝地和西斯用作教学设备或存储有价值的信息。绝地覆灭后，它们成了稀有的、被严密保护的文物。[DaveClarke]造了一个给[房间](https://www.hackster.io/daveclarke/holocron-lamp-for-the-discerning-jedi-0d1f07)照明。

[DaveClarke]围绕粒子光子建造了这种灯——一种基于 STM32 ARM-M0 的微控制器，带有 Cypress wifi 芯片。所有[戴夫]需要的工作是一个红外接近传感器，一个伺服和一束超高亮度的白色发光二极管。当传感器检测到某些东西时，它会启动系统。伺服系统转动齿轮，使灯升起，led 逐渐变暗。下一次传感器检测到什么，伺服降低灯，灯光开始淡出。由于光子与云相连，系统也可以通过网络接口访问。

好吧，这只是一个红外传感器检测反射的红外光，而不是用来打开它的力量，但它仍然很酷。[DaveClarke]的网站上有大量的图片和视频，以及原理图、3D 打印机设计和源代码。整个东西是使用 Autodesk Fusion 360 设计的，在大约 30 个小时内进行了 3D 打印，并压配合在一起。一个非常简单而巧妙的设计。现场还有其他一些很棒的灯，像这个[朵朵花灯](https://hackaday.com/2016/10/11/blooming-flower-lamp-will-test-your-3d-printer/)或者这个激光切割[灯，它也有一个独特的开关](https://hackaday.com/2016/03/18/laser-cut-lamp-with-a-magical-switch/#more-194997)。

 [https://www.youtube.com/embed/F_uzx-iDd_Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/F_uzx-iDd_Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/QiFjHnkQcrE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/QiFjHnkQcrE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

