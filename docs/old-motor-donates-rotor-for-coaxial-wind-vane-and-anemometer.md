# 旧电机为同轴风向标和风速计捐赠转子

> 原文：<https://hackaday.com/2017/01/12/old-motor-donates-rotor-for-coaxial-wind-vane-and-anemometer/>

问题:建立一个组合风速计和风向标，其中两个传感器的枢轴是同轴的。解决方法:[把一个旧的万能电机变成风向标的步进式电位器](http://www.instructables.com/id/COMMUTATOR-BASED-DIRECTION-INDICATOR/)，然后拉几个小把戏就把整个东西组装好了。

我们不得不承认，当我们第一次看到[Ajoy Raman]的 Instructables 帖子时，我们认为他使用了一个通用电机来产生风速表的电压。但是[Ajoy]对同轴问题的解决方案远比这有趣。一个废弃的通用电机捐赠了它的转子和轴承。绕组从组件上被剥去，只留下换向器。1kωSMD 电阻焊接在相邻换向器部分上，形成一个 22kΩ的串联电阻，每 1k 有一个抽头，允许微控制器的 ADC 读取 0 至 2.2V 电压，具体取决于叶片的角度。

虽然很聪明，但[Ajoy]仍然不得不拔掉同轴部分，他只使用钻床从一端到另一端钻出旧电机轴。风速计轴穿过轴上的孔，转动一个小 DC 马达来感应风速。

可能有其他方法来实现这一点，但考虑到这一解决方案的限制和低成本，我们向[Ajoy]脱帽致敬。不过，我们有点担心风速计用的马达。当用作发电机时，可能会产生阻力。也许更好的解决方案是使用霍尔效应传感器来计算硬盘转子的转数。

 [https://www.youtube.com/embed/dcD20cBt2Bs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/dcD20cBt2Bs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

