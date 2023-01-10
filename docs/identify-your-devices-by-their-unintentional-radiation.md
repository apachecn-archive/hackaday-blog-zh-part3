# 通过无意辐射识别您的设备

> 原文：<https://hackaday.com/2016/05/22/identify-your-devices-by-their-unintentional-radiation/>

RFID 本应彻底改变资产跟踪，取代任何地方的条形码。或者至少这是标签价格低于 5 美分时的预测。即使是散装的，它们的价格仍然是 7 到 15 美分，而且条形码仍然很漂亮。迪士尼研究中心的(杰克·杨)和(阿兰森样本)希望改变这种状况。

他们不再给每一个电子设备贴标签，而是使用[设备当前通电时产生的任何电磁辐射](https://www.disneyresearch.com/publication/em-id/)。令人惊讶的不是他们能区分 iPhone 和玩具光剑，而是他们能区分玩具光剑*和*。但是很明显，每一件产品都有足够的制造和公差差异，所以大多数时候它们都是独一无二的。

[纸](https://s3-us-west-1.amazonaws.com/disneyresearch/wp-content/uploads/20160427222554/EM-ID-Tag-less-Identification-of-Electrical-Devices-via-Electromagnetic-Emissions-Paper.pdf) (PDF)经过细节和程序。最酷的一点？他们使用的传感器是 RTL-SDR 单元，去掉了无线电混频器前端，代之以简单的变压器。这使他们能够将基带(从 0 到 28.8 MHz 调谐)直接馈入 ~~DAC~~ ADC，然后馈入执行繁重数学运算的计算机。锯掉一个电视调谐器的前端是一个黑客，对于那些有空宾果卡的人来说。

如果你喜欢统计学，你会想阅读这篇论文，了解他们如何准确地对物体进行分类的细节，但总的来说，他们首先要弄清楚他们“听到”的是哪种类型的设备，然后专注于特定的设备。他们使用的测量结果实际上是一个归一化的相关性。

虽然我们不确定这将如何扩展到数千台设备，但他们从五台设备中选择一台设备的结果非常好(约 95%)。这种方法不会对设备 CPU 的超频或欠频产生影响，所以我们担心温度和电池电压的影响。但这是一个新颖的想法，一个适合黑客重建的想法。对于 RTL-SDR 的价格来说，没有 RFID 系统那样的额外的每标签支出，这是非常简单的。

感谢[静]的提示！Via [Engadget。](http://www.engadget.com/2016/05/05/disney-research-em-id/)