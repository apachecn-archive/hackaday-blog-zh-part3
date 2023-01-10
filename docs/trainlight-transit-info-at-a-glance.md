# 列车之光:交通信息一览

> 原文：<https://hackaday.com/2016/03/14/trainlight-transit-info-at-a-glance/>

在一个感官超负荷的世界里，有时在没有一堆杂乱信息的情况下获得你需要的信息是很好的。[Savage]创造了一个吸引人的极简系统来显示他在旧金山附近的特定列车的当前等待时间。

它基本上是一个火花核心和一条每米 60 个 LED 的 WS2812Bs。一个 1000 F 电容过滤来自开关适配器的功率，一个电阻限制流向 led 的电平转换逻辑。由卡片制成的八道屏障防止亮区一起出血。方形画布面板的侧面指示了主要方向，并且朝向[Savage]朝南的房子。

服务器使用 RESTbus JSON API 每 30 秒获取一次预测数据。[野蛮人]增加了一点时间走下楼梯，穿上鞋，走到每一站。TrainLight 通过 WiFi 接收这些时间，并相应地点亮 led。如果某个区域根本没有点亮，那么该线路的等待时间将超过 10 分钟。深绿色表示你有 5-10 分钟到达那里，浅绿色表示 2-5 分钟。如果发光二极管是黄色的，你最好穿上你的跑鞋。

这是一个相当简单的构建，重点是微妙的。甚至在他家的客人明白他们在看什么之前，[萨维奇]的火车灯就成为了一个有趣的谈话闪光灯，并兼作楼梯照明。休息之后会有一个稍微加速的演示。

想自己做吗？[萨维奇]有一个[教程页面](http://www.outriderindustries.com/trainlight-build-your-own/)和[他的代码在 gits](https://github.com/seanjsavage/TrainLight/tree/master/firmware/trainlight) 上。闪烁的灯光也有助于告诉你[火车是否在运行](http://hackaday.com/2015/05/08/leds-strips-tell-you-the-trains-arent-running/)。

[https://player.vimeo.com/video/120031501](https://player.vimeo.com/video/120031501)