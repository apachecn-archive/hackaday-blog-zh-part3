# 谷歌机器学习变得简单

> 原文：<https://hackaday.com/2017/03/14/google-machine-learning-made-simpler/>

如果你看过机器学习，你可能会注意到很多例子很有趣，但很难理解。这就是为什么[Jostmey]创造了[裸张量](https://github.com/jostmey/NakedTensor?bare)，一个使用张量流的最小例子。例子很简单，只是对一些数据点做一些直线拟合。一个示例展示了如何串行完成，一个示例展示了如何并行完成，另一个示例展示了如何处理 800 万个点的数据集。所有代码都是用 Python 写的。

如果你还没有接触过，TensorFlow 是 Google 的一个开源库。引用其网站上的话:

> TensorFlow 是一个使用数据流图进行数值计算的开源软件库。图中的节点表示数学运算，而图边表示它们之间通信的多维数据数组(张量)。灵活的架构允许您使用单个 API 将计算部署到台式机、服务器或移动设备中的一个或多个 CPU 或 GPU。TensorFlow 最初是由谷歌机器智能研究组织内谷歌大脑团队的研究人员和工程师开发的，目的是进行机器学习和深度神经网络研究，但该系统足够通用，也适用于各种其他领域。

在包括[机器人](https://hackaday.com/2016/10/09/tensorflow-robot-recognizes-objects/)之前，我们已经看到了一些更大的 TensorFlow 项目。当然，机器学习现在非常流行。一本机器学习书籍在[的 Kickstarter 上筹集了超过 25 万美元。我们希望这将是一本真正的好书。](https://www.kickstarter.com/projects/adrianrosebrock/deep-learning-for-computer-vision-with-python-eboo)