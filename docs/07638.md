# 微小张量为 Micros 带来机器深度学习

> 原文：<https://hackaday.com/2017/11/13/tiny-tensor-brings-machine-deep-learning-to-micros/>

我们之前讨论过 TensorFlow 谷歌的深度学习库。处理所有这些数据是大型计算机的职责，而不是嵌入式系统，对吗？没那么快。[Neil-Tan]和其他人一直在研究 [uTensor](https://github.com/neil-tan/uTensor) ，这是一个在支持 Mbed-OS 5.6 或更高版本的板上运行的实现。

Mbed 当然是 ARM 的嵌入式框架，而 uTensor 要求芯片上至少有 256K 的 RAM，一张 SD 卡不到(没错；小于)32 GB。如果您选择的主板还没有 SD 卡插槽，您需要添加一个。

该项目目前正处于紧张的开发阶段。您将需要使用 Mbed 的命令行工具，并期望花一点时间摆弄东西。示例使用 Nucleo F767ZI，它需要 SD 卡突破，但大约 20 美元可能值得从开发人员似乎正在使用的相同板开始。

当然，你也可以在树莓 Pi 上安装 [TensorFlow，但那并不是真正的微控制器。这实际上只是你最终目标的一个函数。很容易想象机器人使用手臂做任何事情，包括高级任务，如](https://hackaday.com/2017/04/11/introduction-to-tensorflow/)[物体识别](https://hackaday.com/2016/10/09/tensorflow-robot-recognizes-objects/)。那是假设它有足够的马力。

顺便说一下，我们的[袖珍信号发生器](https://hackaday.com/2015/09/15/how-to-build-a-pocket-sized-mbed-signal-generator/)项目使用了一个 K64F 板，它有一个 SD 卡插槽和足够的内存。那块板可能是中尉的好目标。