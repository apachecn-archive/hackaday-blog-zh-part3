# 谷歌的《盗梦空间》把这只乌龟当成了枪；图像识别伪装

> 原文：<https://hackaday.com/2017/11/03/googles-inception-thinks-this-turtle-is-a-gun/>

麻省理工学院计算机科学和人工智能实验室[CSAIL]的优秀人员已经找到了一种方法[来欺骗谷歌的 InceptionV3 图像分类器](http://www.labsix.org/physical-objects-that-fool-neural-nets/)，让它看到一只实际上有一只乌龟的步枪。这是通过向分类器呈现所谓的“对手例子”来实现的。

对手的例子是一个经过验证的 2D 斯蒂尔斯的概念。2014 年，[Goodfellow]，[Shlens]和[Szegedy] [给一只熊猫的图像](https://arxiv.org/abs/1412.6572)添加了难以察觉的噪音，从此这只熊猫被归类为长臂猿。这种方法依赖于图像不受干扰，可以通过缩放、模糊或旋转图像来克服。

现实世界恶作剧的适用性受到严重限制，但这改变了一切。这只武器化的海龟是一张彩色 3D 照片，从任何角度看都被算法错误分类了。为了实现这一点，需要一些关于分类器的知识来产生误导性的输入。诸如旋转、缩放和倾斜之类的图像变换以及颜色校正甚至打印误差都被添加到输入中，然后结果被优化以可靠地误导算法。整个过程记录在[CSAIL]关于该方法的[论文](https://arxiv.org/abs/1707.07397)中。

这相当于对机器视觉的伪装。假设这种方法反过来也适用，将枪支(或其他任何东西)伪装成海龟的可能性对自动化安全系统有着严重的影响。

由于这只海龟瞄准了盗梦空间算法，它应该能够骗过 Hackaday 自己的[Steven Dufresne]构建的 DIY[图像识别对话框](https://hackaday.com/2017/06/14/diy-raspberry-neural-network-sees-all-recognizes-some/)。

感谢[亚当]的提示。