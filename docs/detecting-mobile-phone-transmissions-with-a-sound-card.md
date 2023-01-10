# 用声卡检测移动电话传输

> 原文：<https://hackaday.com/2017/06/22/detecting-mobile-phone-transmissions-with-a-sound-card/>

任何在 21 世纪初拥有一套廉价电脑扬声器的人都听过这种声音——GSM 手机大约每小时一次与手机信号塔发出有节奏的嘀嗒嘀嗒声。[，[153armstrong]有一篇关于如何在你的电脑上捕捉这个的文章。](https://thehackerdiary.wordpress.com/2017/05/18/simple-mobile-phone-detector-using-headphone-jack/)

这非常简单——只需将一套耳机插入声卡的麦克风插孔，将手机放在旁边，点击录音，然后等待。耳机线充当天线，当手机传输时，它会在导线中感应出电流，该电流被声卡拾取。

[153armstrong]指出，他们的设置似乎只接收 2G 手机的信号，可能使用 GSM。它似乎不能接收 3G 或 4G 手机的任何信号。我们敢打赌，这是由于不同的蜂窝技术传输方式的差异——让我们知道你在评论中的想法。

该系统作为一种在近距离检测传输电话的方法是有用的，但是由于计算机声卡的有限带宽，它根本无法实际解码传输。至于其他实验，[为什么不用你的声卡来检测闪电](http://hackaday.com/2017/06/10/detect-lightning-strikes-with-audio-equipment/)？