# 用逆日晷表看时间

> 原文：<https://hackaday.com/2017/07/27/tell-time-with-a-reverse-sundial-watch/>

[Xose Pérez]着手制作一款[日晷腕表](http://tinkerman.cat/solr-digital-wrist-watch/)，将磁强计和一个小尼龙螺栓结合在一起，作为日晷的指针，但它并不像你想象的那样工作。你不用磁强计将日晷指向北方，而是调整手表的角度，直到螺栓的影子与 PCB 上的白线匹配，ATmega328P 计算太阳的方位角，从而确定时间。为了显示时间，他使用了 QDSP-6064 气泡显示器，因为日晷是复古的。

他对项目建设的描述包括许多有趣的轶事，比如他试图在放弃和利用 Seeedstudio 的 PCBA 服务之前焊接 HMC5883 磁力计的 LCC 连接。他拿回了 10 块装有 ATmega 和磁力计的板，而剩下的留给[Xose]来填充。

这个项目的一个有趣的细节？没有太阳你看不出现在是什么时间，但是在明亮的阳光下你看不清气泡显示。

如果你正在寻找我们发布的更多手表项目，请查看这款[腕控手表](http://hackaday.com/2016/11/26/controlling-this-smartwatch-is-all-in-the-wrist/)、 [Chronio DIY 手表](http://hackaday.com/2017/02/15/chronio-diy-watch-slick-and-low-power/)和这款很酷的[谢妮电子管手表](http://hackaday.com/2017/01/20/plus-size-watch-with-a-pair-of-tiny-nixies/)。