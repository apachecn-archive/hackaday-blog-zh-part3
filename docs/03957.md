# 将 TP 链路路由器转换为任务控制，实现廉价的 433MHz 家庭自动化

> 原文：<https://hackaday.com/2016/10/26/converting-a-tp-link-router-to-mission-control-for-cheap-433mhz-home-automation/>

[Jean-Christophe Rona]发现自己有了一些空闲时间，并决定完成他两年前开始的一个项目，[逆向工程廉价的 433MHz 家庭自动化设备](http://blog.rona.fr/post/2016/10/22/Home-automation-with-cheap-433MHz-plugs-a-1%24-433MHz-transmitter-and-a-TP-Link-TL-WR703N-router)。他希望远程控制他的空间加热器，为寒冷和现在的机器人冬天做准备。

在前世，他逆向设计了这些廉价的无线插头、车库门和电动百叶窗都使用的协议。这最终导致了一个名为 [rf-ctrl](https://github.com/jcrona/rf-ctrl) 的小库，它可以以正确的方式切换和读取 GPIO 引脚来控制这些对象。他在库中内置了一些更流行的协议，如果你需要的话，他甚至写了一个如何自己进行[逆向工程](http://hackaday.com/2015/02/16/using-matlab-and-sdr-to-reverse-engineer-433mhz-messages/)的指南。

[Jean-Christophe]成功连接了他的空间加热器插头后，着手将一台廉价的 TP Link 路由器改造成他们的指挥中心。由于 TP Link 从未想到有人会将他们的方形钉锤入不匹配的孔中，因此需要小心焊接和一些漆包线来断开 GPIO 引脚，但这完全在平均技能范围内。

最终的结果是一个精致的蓝色盒子，上面挂着一个小小的天线，我们希望它能为即将到来的冬天提供一个温暖的住所。