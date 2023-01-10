# 通过观看音频信号在 VR 中放入风

> 原文：<https://hackaday.com/2017/12/14/putting-wind-in-vr-by-watching-the-audio-signal/>

将物理反馈集成到虚拟体验中的一个简单方法是使用风扇向用户吹风。这个想法以前也做过，粉丝通常是容易的部分。[Paige Pruitt]和[Sean Spielberg]在他们名为 [ZephVR](https://www.kickstarter.com/projects/1089532524/zephvr-real-wind-for-virtual-reality/) 的 Kickstarter 活动(现已取消)中加入了一些东西，其中有两个安装在 VR 耳机上的小风扇。他们的大部分工作是在软件中完成的，该软件观察音频信号中可识别的“风”的声音，并使用这些声音来打开一个或两个风扇作为响应。

使用软件根据音频线索触发粉丝的好处是，整个系统独立于其他一切工作，不需要开发人员和软件来构建对您的项目的支持，也不需要使用其他中间件。不幸的是，不利的一面是，结果只取决于软件选择正确声音并对其采取行动的能力。下面嵌入的是一个简短的视频，展示了一个测试的行动。

 <https://ksr-video.imgix.net/assets/019/026/322/2026659792c70076b22c71519b8c8a06_h264_high.mp4?_=1>

[https://ksr-video.imgix.net/assets/019/026/322/2026659792c70076b22c71519b8c8a06_h264_high.mp4](https://ksr-video.imgix.net/assets/019/026/322/2026659792c70076b22c71519b8c8a06_h264_high.mp4)

左边是一个调试控制台，红色表示风小或无风，绿色表示风大。风扇安装在显示器的顶部，因此响应是可见的。这不是一个演示，但足以看到这个想法的实施，粉丝们单独对从左侧或右侧经过的物体做出反应。

[Sean]和[Paige]取消了他们的活动，尽管达到了资金目标，但他们似乎决定改变方向，专注于创建一个强大的软件 API，而不是钻研硬件生产。与此同时，他们[分享了他们原型硬件的设计文件](https://drive.google.com/drive/folders/1bRnpyrAtDfvwKZrBPVYfM-Fm8B8fesTt)。希望一些供人们试验的软件会紧随其后。

用粉丝来增加虚拟体验并不是什么新鲜事，但是与应用程序交互并不总是一个挑战。例如, [Superfan](https://hackaday.com/2015/01/07/superfan-gaming-peripheral-lets-you-feel-your-speed/) 项目发现，许多赛车和模拟器游戏已经有了可以被定制硬件访问和使用的运动和反馈数据——只要有合适的软件工具。