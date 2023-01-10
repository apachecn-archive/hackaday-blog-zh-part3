# 来自 Raspberry Pi、Google Cardboard 和 Xbox 控制器的 VR 网真坦克

> 原文：<https://hackaday.com/2016/05/12/vr-telepresence-tank-from-raspberry-pi-google-cardboard-and-xbox-controller/>

很高兴看到不同种类的硬件和软件一起投入到一个项目中，允许某人将通常不会放在一起的东西混合成新的东西。[弗雷迪·基洛]用一个他称之为虚拟现实机器人坦克的项目做到了这一点。这是一种远程呈现设备，使用无线 Xbox 控制器来驱动被跟踪的平台，该平台本身由一个 Raspberry Pi 领导。

Pi 在云台上有两个摄像头，这些摄像头都是通过类似谷歌 Cardboard 的设置来瞄准和观察的。一个健康剂量的自由软件将它粘合在一起，允许像视频流(用 [U4VL](http://www.linux-projects.org/modules/sections/index.php?op=viewarticle&artid=14) )和通过无线控制器转向(用 [xboxdrv](http://github.com/martinohanlon/XboxController) )这样的事情。有些部分需要做一些改动——例如，通过打开和定位两个视频窗口*来查看立体摄像机，这样就可以通过耳机镜头看到它们。它不会扭曲图像来解释耳机中的镜头失真，无线范围可能会受到限制，但最终结果似乎足够好。*

坦克由无线控制器驱动，而安装在耳机中的移动电话让用户通过摄像头观看；每当你移动头部环顾四周，手机中的动作感应就会移动这些摄像头。遥控爱好者会认为这个项目本质上与 FPV 模型飞机的设置工作相同(例如，[无人机比赛](http://hackaday.com/2016/02/03/drone-racing-might-just-be-the-next-big-thing/)甚至[雪地雪橇](https://hackaday.com/2015/03/20/uber-cheap-fpv-snow-sled/))，但是这个项目使用了完全不同的硬件和软件工具链。它展示了使用开放工具作为虚拟“管道胶带”的好处，让人们将不同的东西粘在一起测试一个概念。它证明了只要你愿意摆弄，几乎任何事情都可以做成！

 [https://www.youtube.com/embed/z9gSZwVMybc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/z9gSZwVMybc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

