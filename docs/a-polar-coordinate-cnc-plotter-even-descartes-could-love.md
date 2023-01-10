# 一台连笛卡尔都喜欢的极坐标数控绘图仪

> 原文：<https://hackaday.com/2018/04/20/a-polar-coordinate-cnc-plotter-even-descartes-could-love/>

拆开几个旧的 DVD 驱动器，用电缆扎带把它们缝在一起，加上笔和纸，你就有了一个简单的数控绘图仪。它们是有趣的快速而简单的项目，但是它们确实有点像“插头和突突”的一面。但是[一个使用极坐标的数控绘图仪？那需要多一点努力。](https://hackaday.io/project/146270-polar-drawing-machine)

绝大多数 CNC 项目，从简单的双轴绘图仪到大型 CNC 路由器，都倾向于使用笛卡尔坐标系，其中平面上的点通过它们到两个垂直轴上原点的距离来描述。一切都是漂亮的正方形，测量很简单，数学也很容易。[davidatfsg]决定通过选择一个极坐标系统来提升他的 CNC 绘图仪，其中的点被描述为以指定角度从原点延伸一定距离的向量。大多数绘图仪都是由慧鱼零件构建而成，单个线性轴与旋转绘图平台的中心点相交。标准 g 代码在被发送到自定义 Arduino 控制器执行移动之前，由 Java 小程序翻译成极坐标。看看下面的视频；它看起来非常迷人，我们不禁想知道 polar 3D 打印机将如何工作。

极坐标难住你了吗？当然，这可能是对笛卡尔空间的一点调整。然而，它可能是值得的，出现在从[电缆绘图仪](https://hackaday.com/2012/11/16/raspberry-pi-driven-polargraph-exhibits-high-precision-drawing-ability/)到 [POV 坐立不安微调器](https://hackaday.com/2017/11/26/finally-a-fidget-spinner-we-can-love/)甚至到[色彩空间模型](https://hackaday.com/2018/03/30/color-spaces-the-model-at-the-end-of-the-rainbow/#more-299647)的一切事物中。

 [https://www.youtube.com/embed/u6XwKxZuxqk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/u6XwKxZuxqk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

