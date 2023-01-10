# 使用机器学习来识别超级英雄和其他杂项

> 原文：<https://hackaday.com/2016/12/12/use-machine-learning-to-identify-superheroes-and-other-miscellany/>

[Massimiliano Patacchiola]写了这篇关于使用直方图相交算法识别不同对象的指南。[这里是乐高超级英雄](https://mpatacchiola.github.io/blog/2016/11/12/the-simplest-classifier-histogram-intersection.html)。你需要做的只是眼睛、Python、计算机和一点机器学习的魔法。

他很好地介绍了这个想法。你在一张经过适当裁剪和过滤的照片中拍摄一张你想要识别的物体的颜色直方图。然后你把它输入神经网络，训练它通过颜色来识别不同的超级英雄。当你稍后给它一个新的图像时，它会将新图像的直方图与它的模型进行比较，并输出它属于哪个集合的置信度。

知道这一点很有用。虽然许多视觉算法试图对他们看到的东西做出几何断言，但在混合中添加颜色肯定可以帮助你的友好机器人项目识别朋友和敌人。