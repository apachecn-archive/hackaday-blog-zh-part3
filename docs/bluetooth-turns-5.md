# 蓝牙转向 5

> 原文：<https://hackaday.com/2016/12/12/bluetooth-turns-5/>

上周，无线规范蓝牙家族最新最伟大的成员向世界公布:[蓝牙 5](https://www.bluetooth.com/specifications/adopted-specifications) ！什么主要的变化正在酝酿中？阅读[常见问题解答](https://www.bluetooth.com/~/media/files/specification/bluetooth-5-faq.ashx?la=en) (PDF)，或者[深入研究 2800 页的完整规范](https://www.bluetooth.org/DocMan/handlers/DownloadDoc.ashx?doc_id=421043)(更大的 PDF)。

他们的大卖点包括“高达 4 倍的范围，2 倍的速度，8 倍的广播信息容量”，以推动物联网。等等。[Akiba] [通过 Twitter](https://mobile.twitter.com/freaklabs/status/806798361965641728?p=v) 指出，他们通过在“最大输出功率”规格上增加一个额外的零，将最大功率从 10 兆瓦增加到 100 兆瓦，从而将射程增加了四倍。那就行了。

不那么令人不快的消息是，他们还允许更低比特率的模式，这也将增加范围，而不是简单地提高功率。该规范实际上正在改变，让用户工作出他们的功率，范围和比特率的最佳组合。我们同意。但是如果不支付带宽费用，你不可能获得 4 倍的范围和 2 倍的速度。那只是物理学。

如果你在蓝牙低能耗(BLE)中使用信标模式，你会很高兴听到他们将信标包从 31 字节延长到 255 字节，这样你就可以发送更多的数据而不会消耗太多的能量。就是那个“8x”。蓝牙 5.0 也向后兼容蓝牙 4.2，所以如果你不想利用更新的功能，你不必重做任何事情。你目前的 BLE 信标将继续工作。

最后，有一些竞争检测和其他带宽优化正在进行，这在我们拥挤的 2.4 GHz 办公室频谱中是受欢迎的。我们猜测这就是“2 倍速度”的主要来源，但大约有 2，750 页我们还没有阅读，所以如果你正在钻研规范，请让我们知道你在评论中找到了什么。

感谢[秋叶]通过推特向我们透露了这个消息。去看看他在深圳超级电脑展上发表的关于获取黑客资料的精彩演讲。