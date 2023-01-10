# 多边形和圆周率更好的龙卷风预警

> 原文：<https://hackaday.com/2016/11/11/better-tornado-warnings-with-polygons-and-pi/>

每个人都密切关注天气，但对于那些生活在龙卷风盛行地区的人来说，观察天空可能是一件生死攸关的事情。当到达避难所或在户外被抓住之间的差别可能是几秒钟的事情时，建立一个互联网支持的 Raspberry Pi 天气警报系统可能是有意义的。

我们知道你在想什么——为什么不买一个现成的带有特定区域信息编码([同](https://en.wikipedia.org/wiki/Specific_Area_Message_Encoding))报告的天气警报收音机，或者只依赖一个智能手机应用程序呢？正如(吉姆·斯卡伯勒)解释的那样，生活在龙卷风走廊的中心，小时候与悲剧擦肩而过，教会你不要对恶劣的天气自满。他发现了同一个系统的一个问题:县级以下缺乏位置粒度，导致在龙卷风季节倾向于过度警告。[Jim]的构建试图通过整合国家气象局[多边形警告](http://www.nws.noaa.gov/regsci/gis/)来改善这一点，多边形警告将可能出现恶劣天气事件的区域定义为地理顶点的集合，而不是政治单位。他使用的是具有相同解码功能的 Raspberry Pi NOAA 天气无线电接收器，虽然细节很少，而且该项目正在进行中，但其想法似乎是一旦发布县级警告，就使用 Pi 来收集 NWS 站点的多边形数据。

这是一个有趣的想法，我们将继续关注[吉姆]的建设。与此同时，你可以用这个 Arduino 相同的解码器来温习天气广播和相同的编码。

[通过[天气](http://reddit.com/r/weather/comments/5aeop0/build_your_own_raspberry_pi_tornado_warning_system/)