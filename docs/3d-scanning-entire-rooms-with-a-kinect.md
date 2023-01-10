# 用 Kinect 扫描整个房间

> 原文：<https://hackaday.com/2015/12/10/3d-scanning-entire-rooms-with-a-kinect/>

几乎按照定义，最酷的技术和前沿研究都被锁在大学里。虽然这对于博士后和他们的授权写作能力来说很棒，但对于想使用这项技术的人来说，这不是最好的系统。几年前，以及从那以后的很多次，我们看到了一些研究，将 Kinect 变成了用于非常大区域的 3D 地图相机。这是虚拟现实的未来，但许可证和一般知识产权的繁琐手续阻碍了适当的分发。现在，这项技术的源代码，[kincontinuous](https://github.com/mp3guy/Kintinuous)和 [ElasticFusion](https://github.com/mp3guy/ElasticFusion) 都可以在 Github 上获得，免费供所有人(非商业)使用。

我们以前见过几次 kintinu ous——第一次是在 2012 年，展示了用 Kinect 绘制大面积地图的可能性,[绘制了一条穿过建筑物的 300 米长的路径](http://hackaday.com/2013/06/08/3d-mapping-of-rooms-again/)。随着 Oculus Rift 的推出，居住在这些虚拟扫描空间[变得更加酷](http://hackaday.com/2013/06/08/3d-mapping-of-rooms-again/)。如果虚拟现实有未来，我们需要一种方法来捕捉现实生活并使其数字化。到目前为止，这是唯一一个大规模这样做的软件栈

如果你在考虑用一个树莓派在路上带着 Kintinuous，你可能要看看硬件要求。为了获得好的结果，需要非常快的 Nvidia GPU 和快速的 CPU。你也不能将它用于运行 [ROS](http://www.ros.org/) 的机器人；这些软件根本不能一起工作。尽管如此，我们现在已经有了 Kintinuous 和 ElasticFusion 的源代码，而且我肯定有不少人对改进代码并将其引入其他系统感兴趣。

你可以看看下面几个 ElasticFusion 和 Kintinuous 的视频。

 [https://www.youtube.com/embed/XySrhZpODYs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/XySrhZpODYs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/D3yYjaLmiqU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/D3yYjaLmiqU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

