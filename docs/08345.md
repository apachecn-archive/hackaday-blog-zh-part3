# 21 世纪的会说话的钟

> 原文：<https://hackaday.com/2018/01/27/a-talking-clock-for-the-21st-century/>

会说话的时钟服务正在消失，很可能你们中很少有人会意识到它的消失。作为 20 世纪技术的主要内容之一，在廉价的无线电控制时钟(GPS)出现之前，除了每小时的无线电时间信号，会说话的时钟服务是消费者唯一普遍可用的准确时间信息来源。你会拨(当然是在真正的拨号盘上！)一个电话号码，在听到哔哔声后，会有录音通知您时间。时钟设置好了，电话公司赚了一大笔钱，每个人都对他们的高科技音频钟表感到满意。

[Nick Sayer]使用 USNO 主时钟电话来观看新年，但不得不使用来自另一个时区的声音。在太平洋时间，似乎没有服务可以提供了。他对未来一年问题的解决方案？做一个他自己的会说话的钟，一个从 GPS 得到时间参考的钟。

其核心是一个 SkyTraq Venus838LPx 微型 GPS 模块，与 ATMega32E5 微控制器相连。语音以预先录制的样本形式存储在 SD 卡上。有一个小型板载放大器来驱动单个扬声器。为了极端的真实性，也许它可以连接到 GSM 移动电话模块上，以提供拨号服务，但他拥有新年前夕所需的一切。

想听听那种怀旧的感觉吗？看看下面的快速剪辑。至于现代的替代品，过去我们这里至少有一个会说话的时钟，但没有一个使用 GPS 的。

 [https://www.youtube.com/embed/_3cojPDbFYg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/_3cojPDbFYg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



GPS 卫星图片: [NASA【公共领域】](https://commons.wikimedia.org/wiki/File:GPS_Satellite_NASA_art-iif.jpg)。