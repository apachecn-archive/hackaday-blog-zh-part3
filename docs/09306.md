# 超级简单，超级便宜的 FPV 无人机追踪

> 原文：<https://hackaday.com/2018/05/04/super-simple-super-cheap-fpv-drone-tracking/>

当你在比赛中时，有什么比视频信号中断更破坏无人机第一人称视角(FPV)体验的呢？可能什么也做不了，也可能你对此无能为力。还是有？基于 RSSI 的简单追踪器会有助于锁定你的视频信号吗？

老实说，我们不确定它会不会，但我们认为看到[flyerpv]的追踪器跟着他的无人机到处跑是非常漂亮的。这个想法很简单，使用他已经有的全分集 FPV 接收机。分集接收机不断监控来自多根天线的信号强度，以确定监听哪根天线，从而提高接收质量。[flyerpv]将 RSSI 输出发送到 Arduino 上的模拟输入，Arduino 驱动伺服系统，使信号尽可能接近。Arduino 和为其供电所需的 DC-DC 转换器可以很好地安装在接收器外壳中，无需修改，这是一个不错的选择。有了 3D 打印的伺服支架和一些花哨的定向天线，该设置现在可以很好地跟踪他的无人机。请看下面的实际操作。

当然，反应可以更快，我们希望看到另一个接收器和伺服添加到轨道间距以及偏航。对于第一遍，我们认为这很棒，但[flyerpv]应该享受它，以防[AI 很快接管我们的飞行乐趣](https://hackaday.com/2017/11/29/high-speed-drones-use-ai-to-spoil-the-fun/)。

 [https://www.youtube.com/embed/aACTKziuDVE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/aACTKziuDVE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

