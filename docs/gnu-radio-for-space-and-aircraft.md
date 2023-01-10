# GNU 太空无线电(和飞机)

> 原文：<https://hackaday.com/2016/06/10/gnu-radio-for-space-and-aircraft/>

GOMX-3 是一颗立方体卫星，有几个有效载荷。其中之一是软件定义无线电，配置为读取商业飞机发送的 ADS-B 信号。这个想法是卫星可以监视海洋上空的飞机和其他没有雷达覆盖的地方。ADB-S 传输飞机的 ID、位置、高度和意图。

问题是 ADS-B 的射程很短(约 80 海里)。GOMX-1 证明了这些信号可以从轨道上捕捉到。GOMX-3 的能力更强。该卫星有一个螺旋天线和一个 FPGA。

GomSpace 卫星的幕后人员为 ADS-B 数据信标设计了一个完整的解析器，destevez 将其整合到 GNU 无线电模块中。在[德斯特维斯的][博客文章](http://destevez.net/2016/05/gomx-3-data-download/)中，有一个在地图上捕捉数据的很好的表示。如果你想要更少的交互，你可以看到所有收集数据的静态地图。如果你想试着拿起 GOMX-3，你可以在下面的视频中听到它的传输。

我们过去已经谈了很多关于 [CubeSats](http://hackaday.com/2015/12/31/32c3-so-you-want-to-build-a-satellite-2/) 和 [ADS-B 监控](http://hackaday.com/2014/01/16/build-a-cheap-airplane-ads-b-radio-receiving-tracking-station/)(链接断了，但视频还能用)。如果你想要一个 [GNU 电台初级读本](http://hackaday.com/2015/11/11/getting-started-with-gnu-radio/)，我们也已经做了。

 [https://www.youtube.com/embed/we24T9vVhbA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/we24T9vVhbA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

