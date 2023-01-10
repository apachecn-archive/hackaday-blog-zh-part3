# Hackaday 奖参赛作品:OrthoSense，一款用于物理治疗的智能护膝

> 原文：<https://hackaday.com/2017/09/25/hackaday-prize-entry-orthosense-a-smart-knee-brace-for-physical-therapy/>

如果你有膝盖手术，你可能会指望一些物理治疗来配合它。但是有一件事你可能无法指望，那就是从你的治疗师那里得到足够的关注。[Vignesh]的母亲就是这种情况，她患有骨关节炎(OA)。她的理疗师日程繁忙，不能经常去看她，让她对自己的康复进展感到惊讶。

[维格内什]已经对生物工程和可穿戴设备产生了长期兴趣。他母亲的经历使他陷入了对 OA 康复细节的研究。他发现只有不到 35%的患者坚持接受家庭疗法。虽然有很多因素在起作用，但缺乏反馈和强化是关键因素。[Vignesh]试图为病人和治疗师开发一个简单的系统来共享信息。

这项工作的成果是 [Orthosense，这是一个智能膝盖支撑系统，可以测量步态角度、关节声学和关节应变](http://hackaday.io/project/26912-orthosense)。用户戴上支具，将其与设备配对，并完成他们的治疗程序。嵌入支架的传感器通过蓝牙将数据上传到云端。

关节张力是通过一条沿着膝盖延伸的窄条导电织物来测量的。当用户进行锻炼时，织物会拉伸和放松，同时改变阻力。相对于惠斯通电桥分压器测量这些变化。膝盖的步态角度通过 IMU 测量，并相对于臀部角度进行计算，这为应变传感器收集的数据提供了一个参考点。一个驻极体麦克风和一个灵敏的接触式麦克风专为身体声音设计，可以拾取膝盖发出的所有爆裂声和尖叫声。对这些数据的分析提供了对组成关节的软骨和骨骼状况的深入了解。正如你所想象的，不健康的软骨比健康的软骨更吵闹。

[Vignesh]的原型基于 tinyTILE，因为它具有板载 IMU、ADC 和蓝牙。由于 Curie 的所有产品都已停产，下一个版本将使用 nRF52832 或 BC127 模块和单点传感器。[Vignesh]为这个系统设想了很多，我们对所有这些都点头同意。

The [HackadayPrize2017](https://hackaday.io/prize) is Sponsored by:[![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Texas Instruments](img/3734f1c96ffff85ea2a7eaddc92844ba.png)](https://hackaday.io/ti)