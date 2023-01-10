# Arduino +软件定义无线电=数百万辆易受攻击的大众汽车

> 原文：<https://hackaday.com/2016/08/18/adruino-software-define-radio-millions-of-vulnerable-volkswagens/>

正如我们[之前提到的](http://hackaday.com/2015/09/01/the-year-of-the-car-hacks/)，在一个甚至你的汽车都可以连接数据的时代，你的汽车的完整性充其量可能是一个可疑的赌注。针对这些担忧，英国伯明翰大学的一篇[即将发表的论文(PDF)](https://assets.documentcloud.org/documents/3010178/Volkswagen-amp-HiTag2-Keyless-Entry-System.pdf) 指出，自 1995 年以来销售的几乎每辆大众汽车都可以通过 Arduino 和软件无线电(SDR)克隆车辆的密钥卡来被黑客攻击和解锁。

由[Flavio Garcia]领导的研究小组描述了两个主要的漏洞:第一个需要将车辆的密码钥匙与车主钥匙链的信号结合起来才能授权访问，而第二个则利用了上世纪 90 年代实施的几乎古老的 HiTag2 安全系统。前者影响了大众生产线上多达 1 亿辆汽车，而后者将用于雪铁龙、标致、欧宝、日产、阿尔法·罗梅罗、菲亚特、三菱和福特的车型。

这个过程并不像组装 40 美元的电子产品然后开着车离开那么简单。潜在的窃贼必须靠近才能检测到表链的唯一钥匙——尽管他们只需要对那辆车这样做一次！—以及对车辆内部网络的另一半代码进行逆向工程。一个准备充分的小偷可以在一分钟内利用 HiTag2 的漏洞解锁车辆。[Garcia]和他的团队注意到只有大众高尔夫 7 没有被利用。

如果偷窃不是你的事，而你想黑掉你的车，大众仍然有最好的选择，可爱的甲壳虫。

谢谢你的建议，therafman！] Via [ [Wired](https://www.wired.com/2016/08/oh-good-new-hack-can-unlock-100-million-volkswagens/) 。