# 用 DLP 做 PCB，OMG！

> 原文：<https://hackaday.com/2016/01/07/make-pcbs-with-dlp-omg/>

有很多方法可以剥下这只自制多氯联苯猫的皮！这里还有一个。[Nuri Erginer]手头有一个 DLP 投影仪，加上一些缩小光学器件，设法把它变成一个一次性 PCB 曝光器。

如果你以前曾经使用过光致抗蚀剂 PCB 材料，你应该知道这个过程:在透明胶片上打印出你的电路，用敏化的 PCB 覆盖透明胶片，用紫外光曝光一段时间，溶解掉未曝光的抗蚀剂，然后蚀刻。在这里，[Nuri]通过直接从 DLP 投影仪曝光电路板，将前三个步骤合二为一。

问题是投影仪的分辨率限制了你可以制作的电路板的尺寸。以 XGA 分辨率(1024×768)制作一个 10 厘米×10 厘米的电路板，最终在好的方向上的特征尺寸约为 0.004 英寸，在另一个方向上的特征尺寸约为 0.005 英寸。

对于 DIP 器件，这是微不足道的，但对于细间距或小型 SMT 器件，这就不行了。另一方面，对于较小的电路板，最好是 4:3 的比例，它也可以工作。而且因为是一次曝光，所以速度是你打不过的。酷黑，[努里]！

当你需要更高的精确度时，[将紫外激光绑在精确的 2D 机器人上](http://hackaday.com/2014/02/03/laser-based-pcb-printer/)是一个不错的方法，但这需要更长的时间。