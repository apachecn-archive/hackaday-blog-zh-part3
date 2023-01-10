# 手臂神经网络机器人的原型制作、电路板制作和编码

> 原文：<https://hackaday.com/2017/11/21/prototyping-making-a-board-for-and-coding-an-arm-neural-net-robot/>

[Sean Hodgins]称他的三部分视频系列为 Arduino 神经网络机器人,但我们更愿意称之为一个有趣的原型系列，设计一个带有表面贴装部件的电路板，组装它，哦对了，在它上面放置一个神经网络，同时提供大量有用的提示。

在第一部分“原型和设计”中，他用试验板为我们展示了一个原型。最终的机器人不是在 Arduino 上，而是在一个围绕 ARM Cortex-M0+处理器定制的板上。然而，对于原型，他使用了 SparkFun SAM21 Arduino 大小的板，Pololu DRV8835 双电机驱动板，四个光敏电阻，两个电机，一块电池和各种其他部件。

一旦他证明原型可行，他就为他的定制板创建原理图。他没有从零开始，而是去 SparkFun 和 Pololu 的网站上寻找电路板的原理图，并将其融入到自己的设计中。在那里，他讲述了他如何以及为什么从 CAD 程序开始，然后转到 KiCad，在那里他讲述了他的布局方法。

第二部分是关于焊接和组装，从他如何在运输包装中对元件进行分类，到在烤箱中进行回流的技巧，以及修复不在所有焊盘上的桥和部件，包括微处理器。

在第三部分，他编写代码。机器人的目标很简单，逃离光源。他首先在没有马达的情况下测试光敏电阻，然后编写一个程序让机器人害怕光线，这次是用马达。最后，他编写了神经网络代码，但在此之前，他首先给出了神经网络如何工作的合理解释。他承认，你并不真的需要一个神经网络来让机器人逃离光明。但是根据他对机器人使用程序方法和神经网络方法运行的比较，我们认为神经网络方法对程序方法的中间情况反应更好。诚然，可以编写更好的过程化版本，但是有了神经网络，他省去了麻烦，他向我们展示了许多可以重用的成果。

如果你想复制这个，[Sean]提供了一个 [GitHub 页面](https://github.com/IdleHandsProject/makennbot)，上面有 BOM、代码等等。看看下面的三个部分，或者只看你感兴趣的部分。

[Sean]的神经网络是一种使用监督学习进行学习的网络，这是一种通过输入和预期输出的表格进行迭代的方法。相反，如果你想让你的机器人通过在其环境中进行实验来学习，这被称为无监督学习，那么看看[【巴斯蒂】的四足步行机器人](https://hackaday.com/2016/12/11/train-your-robot-to-walk-with-a-neural-network/)。

 [https://www.youtube.com/embed/0D5lcNIEa24?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/0D5lcNIEa24?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/fCmMrSfEsuU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/fCmMrSfEsuU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/97R3TcUh5eI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/97R3TcUh5eI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

