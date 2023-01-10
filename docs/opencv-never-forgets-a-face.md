# OpenCV 永远不会忘记一张脸

> 原文：<https://hackaday.com/2017/12/11/opencv-never-forgets-a-face/>

现在所有很酷的手机都在做面部识别。虽然这听起来像是一项大工程，但是如果您能够支持 OpenCV 库，您可以轻松地将人脸检测和识别添加到您的项目中。[LinuxHint]有一个很棒的[教程，让你从 OpenCV 的基础一步步走到实际获取和识别人脸](https://linuxhint.com/opencv-face-recognition/)。它是针对 Ubuntu 用户的，但是代码也适用于任何 OpenCV 支持的平台。你也可以从[DanishMalhotra]看到一个不太详细的教程来了解更多关于[在 Pi Zero 上安装 OpenCV](http://www.instructables.com/id/Face-and-Eye-Detection-With-Raspberry-Pi-Zero-and-/)。

当然，任何面部识别系统都需要一个摄像头。第一个教程的好处在于它假设您对 OpenCV 一无所知，因此它涵盖了使用 face 相关库的基础知识。

人脸识别需要完成两个不同的操作。第一种是简单地识别图像包含人脸。有时这本身就很有用(例如，[自拍相机](https://hackaday.com/2014/11/12/nothings-as-vain-as-a-phone-taking-a-selfie-of-itself-with-itself/)或类似 Snapchat 的滤镜)。OpenCV 提供了哈尔级联人脸检测器，它使用一些[哈尔分类算法](https://en.wikipedia.org/wiki/Haar-like_feature)来快速找到图像中的模式。

一旦你找到一张脸， [Eigenfaces](https://en.wikipedia.org/wiki/Eigenface) 可以通过将区域与已知的人脸类型数据库进行匹配来识别它。本教程讨论了几个您可以使用的数据库。

你拥有的积木越多，就越容易做出令人印象深刻的项目。OpenCV 当然是一个高性能的构建模块。如果你想在更小的东西上做特征脸算法，它[当然是可能的](http://people.ece.cornell.edu/land/courses/ece4760/FinalProjects/s2011/bjh78_caj65/bjh78_caj65/index.htm)。