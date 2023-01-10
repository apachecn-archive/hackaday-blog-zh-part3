# 良好的 USB–用两个微控制器保护您的端口

> 原文：<https://hackaday.com/2017/03/02/good-usb-protecting-your-ports-with-two-microcontrollers/>

如果你需要一个例子来说明为什么不应该把随机的 USB 外围设备插入你的电脑，你只需要看看 BadUSB。[bad USB 攻击](http://hackaday.com/2014/10/05/badusb-means-were-all-screwed/)依赖于每个 USB 设备内部的微控制器是一个黑盒这一事实。如果你将一个 USB 拇指驱动器插入你的计算机，微控制器可以快速设置一个额外的网络接口，将你的所有流量转发到攻击者的服务器，并仍然保持在驱动器上提供所有这些文件和文档。你想要一个每个文件都带病毒的 u 盘吗？坏的 USB 可以做到这一点。

到目前为止，还没有针对使用 BadUSB 实现的设备的治疗或修复方法。[罗伯特·菲斯克]刚刚推出了第一个预防性 USB 设备，旨在防止 BadUSB 进入你的电脑。他称之为 USG，它基本上是 USB 设备的硬件防火墙。

系统的基本设计是这样的:用一个带 USB 主机端口的 ARM 微控制器，用另一个带 USB 设备端口的微控制器，让这些设备通过 SPI 相互通信。这两个微控制器之间的命令协议非常简单，因此减少了攻击面。

[Robert]正在构建 USG 加密狗，但本着开放硬件和可验证硬件的精神，他还发布了基于两个连接在一起的开发板的设计。这个 DIY 版基本就是两块 STM32F4 的 dev 板用 bodge 线砸在一起。总成本-不包括焊料和一个 JTAG 编程器-大约是 50 美元。不，它看起来不像[Robert]的商业版 USG 那么漂亮，但它的作用是一样的，让你的电脑免受 BadUSB 设备的攻击。