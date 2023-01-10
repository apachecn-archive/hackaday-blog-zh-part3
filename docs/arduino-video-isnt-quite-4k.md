# Arduino 视频不太 4K

> 原文：<https://hackaday.com/2017/01/23/arduino-video-isnt-quite-4k/>

视频分辨率一直在提高。640×480 视频的时代已经让位于 720、1080 甚至 4K 分辨率。看不到尽头。然而，你需要很大的马力来处理这么多的像素。如果你有一个由微控制器(可能是 Arduino)驱动的小型机器人，并且你想让它拥有视觉，那该怎么办？你无法用一个小处理器真实地处理高清视频，甚至低级视频。CORTEX systems 有一个开源解决方案:一个带 I2C 接口的 7 像素[摄像头](https://www.openhardware.io/view/312/Snail-Vision-7-Pixel-RGB-I2C-Camera)。

SNAIL Vision 的文件包括物料清单和 PCB 布局。有用于 Vishay 传感器的[软件](https://github.com/thewknd/VEML6040)和使用胶水将镜头支架安装到 PCB 上的规定。这个设计相当简单。除了传感器阵列，还有一个 I2C 多路复用器，它还可以充当电平转换器和一些电阻和连接器。

七个像素够用吗？我们不知道，但我们希望看到一些使用 SNAIL Vision 板或其他低分辨率光学传感器与低端微控制器的例子。这似乎是一个比 Pixy 更便宜的机制。如果七个像素太多，你可以试试[一个](https://hackaday.com/2015/01/31/a-single-pixel-digital-camera-with-arduino/)。

谢谢[保罗]的提示。