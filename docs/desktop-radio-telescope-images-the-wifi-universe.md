# 桌面射电望远镜拍摄 WiFi 宇宙

> 原文：<https://hackaday.com/2018/06/20/desktop-radio-telescope-images-the-wifi-universe/>

这是一个充满了断断续续的项目，它几乎以“本周失败”的功能结束，但我们很高兴地报告,[思想商场]的桌面 WiFi 射电望远镜终于工作了。这真是太酷了。

如果你像我们一样一直在跟踪这个建造，你会知道这源于[一个以前的、更大的射电望远镜](http://hackaday.com/2017/03/23/see-satellites-with-a-simple-radio-telescope/)，【贾斯汀】用它来观测地球同步数字电视卫星星座。这一次，他将目光放在了离家更近的地方，建立了一个系统来可视化 2.4 GHz 的 WiFi 频段。一个简单的螺旋天线安装在步进驱动的方位角-仰角扫描仪上。HackRF SDR 和 GNU Radio 构成了接收机，它只是在天线扫描时捕获每个点的接收信号强度指标(RSSI)值。然后，数据被处理成代表接收到的 WiFi 信号强度的颜色，并放置在扫描区域的光学图像上。第一张图片清楚地显示了几个热点，包括一个以前不知道的路由器。一次室外扫描显示有大量的路由器，尽管这需要更多的魔法来完成。

下面的视频详细叙述了整个故事；如果你必须的话，跳到第三部分，但代价是错过一些有价值的经验和一些很酷的技巧，比如使用扁平的 Schedule 40 管道作为建筑材料。我们希望很快看到这个项目的更多成果，并想知道这个 FPV 赛车无人机追踪器是否能为扩展提供一些有用的提示。

 [https://www.youtube.com/embed/o6WHhqDHSQ4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/o6WHhqDHSQ4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/VABeN4uv03s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/VABeN4uv03s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/g3LT_b6K0Mc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/g3LT_b6K0Mc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

