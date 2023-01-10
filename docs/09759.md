# 测试设备的自制校准

> 原文：<https://hackaday.com/2018/06/15/homebrew-calibration-for-test-equipment/>

如果你在一家大公司工作，你可能有定期校准的测试设备。一些公司有自己的计量实验室，其他公司则外包给外部实验室。在车库实验室，你不太可能进行校准，根据我们的经验，这通常不是问题。尽管如此，至少能够对你的装备进行一次健康检查还是不错的。此外，如果你买了旧的测试设备，并修复它，这将是很好的能够检查它，以及。[IMSAI guy]建立了他自己的[小校准设置](https://www.youtube.com/watch?v=VoXyQsBx2LU)，多年来不断增加，他在最近的一个视频中分享了细节，你可以在下面看到。

该板最初只是一个稳压器和一些 0.01%电阻。然而，随着时间的推移，他增加了一些额外的功能。该设置无法与可追踪 NIST 的实验室设置相媲美，但对于你的车库来说，它已经非常好了。

调节器实际上是现成的精密基准电压源 IC，因此它们应该比您的旧基准电源更好。然而，我们不认为你真的想盲目地复制这种设计，但在电路板上有一个单一的校准套件的想法是可以从你的垃圾箱和 hamfest 发现有机增长的。

电路板上增加了一个来自旧 GPS 的精密振荡器模块和第二个基准电压源。初始基准电压源是一个 10V 器件，室温下的最大误差为+/- 0.05%。不过，他可能想在设备上安装一些二极管保护装置，因为反向接线会破坏它。从好的方面来看，这促使他去寻找更好的新设备。

因此，在更换基准电压源时，他还添加了一个 AD587 作为第二个 10V 基准电压源，它同样精确，并且能够调整输出(尽管他没有使用这一功能)。

当然，如果你痴迷于校准，你可能会想要一个[铷](https://hackaday.com/2015/05/27/measuring-accuracy-of-rubidium-standard/)标准——事实上，视频中就出现了一个。还有各种各样的[精密电阻](https://hackaday.com/2016/03/19/standard-resistor-teardowns/)，我们过去已经看过了。

 [https://www.youtube.com/embed/VoXyQsBx2LU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/VoXyQsBx2LU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

