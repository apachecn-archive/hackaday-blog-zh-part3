# Hackaday 奖参赛作品:Visioneer 传感器平视显示器

> 原文：<https://hackaday.com/2017/09/28/hackaday-prize-entry-visioneer-sensor-hud/>

只有大约百分之二的盲人或视力受损者使用导盲犬和辅助拐杖，他们有自己的局限性。有一些可穿戴设备可以获取传感器数据，并将世界变成视力受损者可以理解的东西，但这些设备很贵。[Visioneer](https://hackaday.io/project/26863-visioneer)是一款可穿戴设备，旨在作为一个传感器包，为视力受损者提供便利。关键特征:它真的很便宜。

Visioneer 由一副太阳镜、两个摄像头、传感器、一个 Pi Zero 和用于音频和振动反馈的骨传导传感器组成。Pi 监听一个 3 轴加速度计和陀螺仪、一个用于 6.5 英尺内障碍物检测的激光接近传感器和一对 NOIR 摄像机。这些数据由神经网络和 OpenCV 进行处理，为佩戴者提供运动检测和物体识别。一块 2200 毫安的电池为它提供动力。

当加速度计确定该人正在行走时，软件切换到避障模式。然而，如果佩戴者站着不动，视觉者会假设你正在与附近的物体互动，利用物体识别软件和触觉/音频线索来传递信息。这是一个很棒的设备，与大多数商业版本的“基于眼镜的物体检测”设备不同，这个项目的 BOM 成本仅为 100 美元左右。即使你把它增加一倍或两倍(你应该这样做)，这仍然是一个数量级的成本降低。

The [HackadayPrize2017](https://hackaday.io/prize) is Sponsored by:[![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Texas Instruments](img/3734f1c96ffff85ea2a7eaddc92844ba.png)](https://hackaday.io/ti)