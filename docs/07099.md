# 便宜又简单的运动跟踪

> 原文：<https://hackaday.com/2017/09/17/cheap-and-easy-motion-tracking/>

[Koppany Horvarth]着手为虚拟现实创造一个非常便宜的光学跟踪装置,它只使用两个摄像头和一定数量的数学运算来完成任务。他知道理论上他可以做到，而且不会花很多钱，但仍然需要大量的工作和略显荒谬的数学量。

在摆弄他设置的用于运行对象跟踪 Python 脚本的网络摄像头时，他发现他的设置倾向于显示一个半透明的对象，其中有一个 LED 作为纯净的褪色白色。这给了[Koppany]一个想法，他可以使用这样的光作为他的目标跟踪项目的一部分。他用透明的 PLA 3D 打印出 50 毫米的空心球，通过 LED 照明，由从旧 USB 电缆上截取的 5V 电源供电。在处理了一些镜头光晕后，他用砂纸将 PLA 打磨了一点来漫射光线，效果非常好。

要了解更多信息，请查看他的 GitHub [代码库](https://github.com/koppanyh/VR-optical-tracking)。你也可以从我们过去发表的一些其他运动跟踪帖子中获得灵感，比如用 PIC 廉价的[运动跟踪和这个](https://hackaday.com/2014/02/13/motion-tracking-on-the-cheap-with-a-pic/) [OpenCV 气枪炮塔](https://hackaday.com/2017/08/04/opencv-turret-tracks-motion-busts-airsoft-pellets/)。