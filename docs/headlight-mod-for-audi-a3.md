# 奥迪 A3 的前灯模块

> 原文：<https://hackaday.com/2018/05/24/headlight-mod-for-audi-a3/>

如果你有一辆上了年纪的车，它可能会缺少一些最新款的装饰和功能。[Muris]有一辆稍微过时的奥迪 A3 8P，它没有自动设置前灯。在较新的车型中，当环境光线低于阈值水平时(阴天条件下或通过隧道时)，或者当挡风玻璃刮水器打开时，该功能会打开前照灯。光传感器集成在后视镜后面的一个特殊支架上，如果他选择工厂改装，需要昂贵的挡风玻璃升级。相反，他决定为他的奥迪 A3 制造自己的[自动前灯传感器升级。](https://www.elektronika.ba/870/automatic-headlight-sensor-mod-for-audi-a3-8p/)

他的当地法规要求当车辆行驶时，车前灯必须一直亮着。因此，乍一看，增加这一功能似乎没有实际意义。但是[Muris]将前灯编程为在白天条件下以 70%供电，当他的传感器检测到低环境光条件时切换到 100%。在省电模式下，所有其他非必要的灯(牌照灯、尾灯)也被关闭，以延长它们的寿命。他通过使用 VCDS ( [VAG-COM 诊断系统](http://www.ross-tech.com/vag-com/))实现了这一目标，这是一款广泛用于大众-奥迪集团车辆的售后诊断工具。他的微型电路在两种电源设置之间切换灯光。

他的计划是在不以任何方式干扰原有线路或灯开关组件的情况下安装该装置。低功率设备由 PIC 微控制器、用于光感测的 LDR(光敏电阻器)和在两种模式之间切换的低电流继电器组成。设置电路切换输出的阈值是通过一个可变的 trimpot 来调整的，该 trimpot 与 LDR 一起充当分压器。[Muris]连接了一个短的定制线束，让他在默认灯开关和汽车电子设备之间安装这个电路。打开电源后，他有 15 秒钟的时间通过切换灯开关 5 次来启用或禁用他的装置，并且该状态被存储在存储器中。微型板使用 SMD 器件组装，并采用热缩套管保护。这条赛道可以和很多其他的车一起很好地工作，所以如果你有一辆可以做这种功能升级的车，那么[Muris]可以在他的博客上下载 Eagle CAD 文件和代码。

看看下面的视频，他运行了一个演示，详细描述了他的电路，然后开始组装 PCB，没有使用老虎钳或第三只手拿着 PCB。他在 00:50 时戴的手表很漂亮。

 [https://www.youtube.com/embed/K3vOIm34mOM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/K3vOIm34mOM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

