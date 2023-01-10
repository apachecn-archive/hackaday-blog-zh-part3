# 免执照网络雄心勃勃

> 原文：<https://hackaday.com/2016/03/20/licence-exempt-network-has-high-ambitions/>

可以肯定地说，物联网是当今热门词汇之一。最近一次看到它在 Gartner 炒作周期中迅速上升到膨胀预期的顶峰，似乎这些天你遇到的每个初创公司都试图在他们的产品中加入物联网元素。在所有宣传的背后，隐藏着一些有趣的无线技术，它们可以廉价地让非常小的微处理器相互通信，并与更广阔的世界通信。

今天，我们想让您关注另一项无线技术，从事这一领域工作的黑客读者可能会对此感兴趣。UKHASnet 是英国高空气球社区开发的无线网络，在欧洲使用廉价的免执照 868MHz 无线电模块，在美洲使用 915MHz 无线电模块。他们正在使用的模块具有令人惊讶的 100mW 的许可证豁免套件可用功率输出，因此该系统被设计为可扩展性和通过安装在气球、多旋翼甚至海上浮标上的节点进行桥接。

所有的 UKHASnet 数据包都以人类可读的明文 ASCII 形式发送，系统[借用了业余无线电的 APRS](https://ukhas.net/wiki/network_structure) 的一些特性。所有的包都被认为是不可靠的，所有的节点重复它们接收的包，并附加上它们自己的节点 ID，并且有网关节点使包可用于因特网。[每个数据包中都有一个重复的数字](https://ukhas.net/wiki/packet_format)来阻止数据包无限继续。

[构建节点是一个简单的过程](https://ukhas.net/wiki/building_a_ukhasnet_node)，只需要无线电模块、微控制器和电池。作为例子，他们为 Arduino 提供了[实现，为 LPC810 微控制器](https://ukhas.net/wiki/guides:arduino_design)提供了[实现。他们的](https://ukhas.net/wiki/guides:lpc810_design)[首选无线电模块是 HopeRF RFM69HW](https://ukhas.net/wiki/radio_hardware) ，但是该系统将能够在同类型的其他模块上运行。

到目前为止，UKHASnet 人员已经在 65 公里的范围内验证了该系统，[在海上创建了节点](http://jamescoxon.net/?p=69)，将其连接到四轴飞行器，并在[建造了一系列其他节点](https://ukhas.net/nodeList)。

这个网络不同于它的商业对手，因为它没有专有知识产权，也没有标准机构的许可。尽管有这个名字，你不必在英国使用它。所有的数据都是清晰的，因此你可能不会在大众市场的商业产品中看到它。但正是这些特点可能使它对创客社区具有吸引力。您的抄写员可能不是唯一一个离开本文，建议他们的本地 hackspace 为 UKHASnet 节点找到空间的人。

这是我们第一次在 Hackaday 展示 UKHASnet。然而，大量使用免许可证无线电模块的项目已经出现在这些页面上，包括[这个用于模型飞机的超远程遥控器](http://hackaday.com/2008/05/08/long-range-rc-on-868mhz/)和[这个气象站传感器网络](http://hackaday.com/2015/08/24/build-a-sensor-network-around-a-weather-station/)，如果它的创造者手头有它，它可能会发现 UKHASnet 很有用。