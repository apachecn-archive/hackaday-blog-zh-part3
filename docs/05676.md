# 乙醇驱动的 Arduinos

> 原文：<https://hackaday.com/2017/04/19/ethanol-powered-arduinos/>

遵循 YouTube 悠久的传统，在网上订购便宜的东西，并在相机运行时玩它，[蒙他·埃尔金斯]买了一台斯特林发动机，驱动 DC 马达用作发电机。这东西仅靠变性酒精能提供多少电力？(会融合吗？)

答案可能不是真正的剧透:它产生的足够在一个普通的 Arduino 上运行“Blink.ino ”,至少当直接通过 5 V 轨供电时。[蒙他]记录了大约 5 V 的开路电压，和在测量的几百毫伏下大约 100 mA 的短路电流。虽然他没有记录足够的中间点来制作真正的功率曲线，但我们猜测发电机可能更适合 3.3 V 电子设备。真正的问题是它是否能处理 ESP8266 的峰值需求。确实是严肃的问题！

这个视频有点长，但当[蒙他]试图用融化的冰块给冷的一面降温时，他的桌子上有一个明火在燃烧，这一幕弥补了这个视频的不足。这自然让我们思考。如果你只有两台斯特林发动机(T1)…(T2)

 [https://www.youtube.com/embed/ukfB5cGwQXk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ukfB5cGwQXk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

