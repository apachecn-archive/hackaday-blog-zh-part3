# 对宜家的新型智能灯泡进行逆向工程

> 原文：<https://hackaday.com/2017/02/06/reverse-engineering-ikeas-new-smart-bulbs/>

在瑞典、捷克、意大利和比利时，宜家推出了新的“智能”灯泡系列。这些国家显然是这些灯泡的测试市场，它们很快就会登陆美国海岸。这意味着智能宜家灯泡将很快随处可见，灯泡网络是一个值得探索的好东西。[Markus]得到了其中的一些灯泡，[现在正在挖掘它们的内部工作机制](https://www.heise.de/make/artikel/Ikea-Tradfri-Das-steckt-im-Smart-Home-aus-dem-Moebelhaus-3597295.html)(德国制造杂志，有一个[谷歌翻译](https://translate.google.com/translate?sl=de&tl=en&js=y&prev=_t&hl=en&ie=UTF-8&u=https%3A%2F%2Fwww.heise.de%2Fmake%2Fartikel%2FIkea-Tradfri-Das-steckt-im-Smart-Home-aus-dem-Moebelhaus-3597295.html&edit-text=&act=url)，其中包括短语‘雀跃的梨’)。

这些宜家灯泡目前有四个版本，从为轨道灯设计的 400 流明灯泡到可能适用于美国爱迪生灯座的 980 流明灯泡。这些灯通过遥控器控制，通过打开灯，将遥控器靠近灯泡，并按下按钮，每个单独的灯泡都与遥控器配对。

这些灯泡内部是一个支持 ZigBee 的硅实验室微控制器，12 个芯片 led 和相关的电子设备，看起来它们可能会通过 [bigclivedotcom](https://www.youtube.com/user/bigclivedotcom/videos) 烟雾测试。在拆开这个灯泡并将无线模块牢固地植入试验板后，[Markus]发现他可以简单地通过点击遥控器来调暗一对 led。在这些灯泡的某个地方，有做一些事情的可能性。

与所有物联网一样，我们必须问一个重要的问题:它会成为天网的一部分，并像去年夏天网络摄像头一样关闭互联网吗？在这方面，这些宜家灯泡看起来相当安全，因为灯泡牢牢地绑在遥控器上，必须靠近灯泡进行配对。我们确信这些灯泡还有一些更有趣的用途，所以一旦[它们在美国](https://fccid.io/FHO-E1526)发布，我们就来看看它们。