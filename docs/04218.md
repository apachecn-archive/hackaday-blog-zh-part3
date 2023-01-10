# 三明治机器人让你吃饱，所以你可以继续黑客

> 原文：<https://hackaday.com/2016/11/27/sandwich-robot-keeps-you-fed-so-you-can-keep-hacking/>

食物。一个必要的——通常是美妙的——中断你正在进行的任何项目。叫外卖变得很贵，而且只吃披萨通常是不健康的。有了 [Sandwich-O-Matic](https://devpost.com/software/sandwich-o-matic) ，一个简单的语音命令就能满足这种生理需求，对你的构建时间影响最小。

这个三明治机器人是为 36 小时的黑客马拉松而建造的，由一个光子和一个 Arduino 控制。后端运行 node，托管在 AWS 上，Google Cloud 用于语音到文本识别。这是一个全自动的声控三明治制作站。DC 电机为烤面包机服务，而装置的其余部分由伺服系统驱动。只需点击网站上的“开始录制”按钮，告诉它你的配料选择，它就开始了。

 [https://www.youtube.com/embed/F9EkMRwM4CI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/F9EkMRwM4CI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



尽管 I2C 和重建他们的分配器设计有一些挑战，他们设法提前完成了建设。未来的版本将包括更多的浇头选择，调味品选择，以及更简化的语音到三明治的过程。

然而，如果你喜欢玩你的食物，那么尽一切办法把它变成一辆遥控汽车。

【感谢提示，Nils Hitze！]