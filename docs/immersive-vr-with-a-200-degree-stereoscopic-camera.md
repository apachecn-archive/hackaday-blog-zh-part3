# 带有 200 度立体摄像机的沉浸式 VR

> 原文：<https://hackaday.com/2017/10/29/immersive-vr-with-a-200-degree-stereoscopic-camera/>

虚拟现实正在流行，但加入虚拟现实需要高昂的前期成本。Hackaday.io 用户科林·佩特(Colin Pate)觉得，即使是最便宜的商用 360 度 3D 相机，800 美元也太贵了，所以他想:“为什么不让我的[以一半的价格拥有](https://hackaday.io/project/26974-vr-camera-fpga-stereoscopic-3d-360-camera)？”

[Pate]知道他需要大量的带宽和许多 GPIO 端口用于摄像头阵列，所以他找到了 Altera Cyclone V SOC FPGA 和 Terasic DE10-Nano 开发板来托管它。目前，他的钻机上有四台 Uctronics OV5642 摄像机，选择这些摄像机是因为它们提供了大量的文档和支持。相机底座本身是一个 3D 打印的八角形，因此八个 OC5642 可以拍摄完整的 360 度照片。

下一步:制作图像！

[Pate]通过将每台相机相隔 64 毫米(人双眼之间的平均距离)安装，并混合每台相机的重叠视野，来实现立体效果。对他来说不幸的是，直到购买了第三轮镜头，他才找到一套有效的镜头——尽管在校准镜头和编程技巧方面做了一些努力，以确保图像能够正确拼接。到目前为止，[Pate]已经成功拍摄了 200 度的立体图像，我们很高兴看到完整的成品！

有很多方法可以只用一台相机捕捉立体图像，但它需要[一个小烟雾和镜子](https://hackaday.com/2010/09/08/steroscopic-rig-requires-only-one-camera/)、[或者在这种情况下](https://hackaday.com/2010/01/14/spherical-and-stereoscopic-photography/)，两个巧妙安装的带鱼眼镜头的相机。