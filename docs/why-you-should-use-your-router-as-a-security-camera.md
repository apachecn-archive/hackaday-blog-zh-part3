# 为什么您应该将路由器用作安全摄像头

> 原文：<https://hackaday.com/2017/11/28/why-you-should-use-your-router-as-a-security-camera/>

一个家庭安全摄像头可以让你安心，并在你不在的时候监视你的房子。目前流行的选择是一个基于 IP 的设备，通过以太网或无线连接到您的家庭路由器，可以访问互联网。但是，如果你可以省去中间人，而是把你的路由器本身变成安全摄像头呢？[【弗雷德】在这里向我们展示如何做到这一点](http://www.fredericb.info/2017/11/netgear-nighthawk-r7800-add-usb-camera-support-to-create-a-security-webcam.html) [。](http://www.fredericb.info/2017/11/netgear-nighthawk-r7800-add-usb-camera-support-to-create-a-security-webcam.html)

黑客首先解析原始路由器的固件。通过简单的文本搜索，发现了一个允许 telnet 访问路由器的调试页面。这提供了对根 shell 的访问，允许完全控制运行该节目的 Linux 系统。

备份好一切后，[【Fred】从 Netgear](https://github.com/frederic/netgear-R7800-GPL) 抓取源代码，重新编译了支持 USB 视频和 Video4Linux2 的内核。这允许路由器与标准 USB 网络摄像头对话。然后，使用 opkg 安装软件来设置路由器，以便在检测到运动时记录视频，这是一件简单的事情。

总的来说，这相当简单，但[弗雷德]想出了一个巧妙的转折。因为路由器本身充当安全摄像头，所以他能够设置摄像头，仅当他的智能手机(以及[Fred]本人)不在家时才启动摄像头。这可以防止录制[Fred]在房子里走动的镜头，从而允许路由器出于安全目的只录制重要的镜头。

用路由器做大事是可能的——不管怎样，大多数路由器只是运行 Linux 的小盒子。看看这个被用作在线能量计的。