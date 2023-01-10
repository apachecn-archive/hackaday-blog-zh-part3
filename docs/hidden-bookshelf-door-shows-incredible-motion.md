# 隐藏的书架门展现出难以置信的动感

> 原文：<https://hackaday.com/2017/01/21/hidden-bookshelf-door-shows-incredible-motion/>

谁小时候没梦想过房子里有一扇暗门或秘密通道？我们中的一些人仍然这样做！[SPECTREcat]已经在一个功能齐全的书柜中建造了一个秘密的门，它有一个独特的开启机制。有趣的机制允许门在铰接到隐藏空间之前，从彼此稍微远离滑动开始。然而，它们的操作是手工的。下一步是[用电子设备自动化秘密开门机制](http://www.instructables.com/id/Electro-Mechanical-Control-of-Hidden-Bookcase-Door/?ALLSTEPS)。

project brain 是一个现成的 Arduino Uno，配有一个 MultiMoto Arduino shield，用于驱动 4 个渐进式自动化 PA-14 线性致动器。这些线性致动器具有 50 磅的力，允许门在 10 秒内完全打开或关闭，并保持不会将书从书架上摔下的速度。

不想在书架上钻一个开关或其他打开机制的孔，[SPECTREcat]增加了一个簧片开关，它由 DVD 封面激活，里面有一个磁铁。除此之外，如果两个小时内没有检测到任何活动，房间内部有一个 PIR 传感器可以自动关门。别担心，里面还有一个手动开关以防万一。

用架子上的一个物品来触发秘密通道是经典之举。他也可能使用了一个秘密的敲门密码，就像我们过去报道的秘密阁楼图书馆的门一样。看看下面的视频，看看铰链和滑动的动作。

 [https://www.youtube.com/embed/KuLo43NcuMI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/KuLo43NcuMI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

