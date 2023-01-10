# 将光纤控制添加到您的 CNC 中

> 原文：<https://hackaday.com/2016/03/20/add-fiber-optic-control-to-your-cnc/>

数控机床可能会非常吵，我们不是在谈论那种你可以用耳塞解决的噪音问题。由于所有这些步进电机和驱动器都可能高速运行，电气噪声往往会干扰您的控制信号。如果您的控制器通过长电缆线路与机器分离，这一点尤其正确。

[但是电噪声不会干扰光束](https://hackaday.io/project/10087-toslinkcnc)！[Musti]和他在 [IRNAS](http://irnas.eu/) 的黑客伙伴决定使用商品[连接](https://en.wikipedia.org/wiki/TOSLINK)电缆和发送器/接收器设备来制作一个便宜且可黑客攻击的光纤系统。基本思想是用光纤在控制板和电机驱动器之间搭桥。要做到这一点，需要传递两个信号:脉冲和方向。他们已经设置了系统，所以它也可以被锁住。为了提高速度和可靠性，数据的序列化、曼彻斯特编码和接收解码都由 CPLDs 处理。

这个团队已经在这个项目上工作了一段时间。如果你想了解更多的背景，你可以看看他们最初的设计想法。这个发布版本[的设计文件在 GitHub 上。](http://irnas.eu/goodenoughcnc/2015/06/05/optical-cnc-control-toslink)一项提议的改进是加入双向通信。双向通信将允许限位开关状态等数据通过光纤从机器传回控制器。

这个光学接口服务于[一个开源的等离子切割机设计](http://goodenoughcnc.eu/applications/)，它本身就很酷。如果 IRNAS 集团听起来很熟悉，那可能是因为我们最近[报道了他们雄心勃勃的千兆以太网项目。](http://hackaday.com/2016/03/10/gigabit-ethernet-through-the-air/)