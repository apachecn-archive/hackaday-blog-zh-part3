# 开源电机控制器实现平滑移动，具有防齿槽效应

> 原文：<https://hackaday.com/2017/11/07/open-source-motor-controller-makes-smooth-moves-with-anti-cogging/>

大约两年前，一个研究小组表明，有可能从廉价的无刷 DC 电机获得精细的电机控制。通常这是不可行的，因为电机是以这样的方式内置的，即对于电机的每个位置，所施加的扭矩是不均匀的，这种现象被称为“齿槽效应”。这对于不需要低速控制的东西来说很好，比如风扇电机，但对于机器人来说更重要一点。自从那个团队发表了他们的成果，我们开始看到[其他人实现他们自己的低速无刷电机控制器](https://discourse.odriverobotics.com/t/anti-cogging-feature/293)。

实现防齿槽效应的新方法绘制出了电机轴任何位置所需的保持扭矩，因此该信息可以在以后使用。当然，这需要大量的校准；[madcowswe]报告称，这种方法需要大约 5-10 分钟的校准时间。[madcowswe]还对他的电机进行了分析，以显示这些波形中包含多少谐波成分，这有助于理解这种现象是如何产生的，以及如何消除这种现象。

虽然[madcowswe]计划为这种电机控制算法添加更多功能，如反向映射、基于速度的缩放和更好的内存使用，但这是一个很好的实现，与普通电机相比有明显的改进。[如果你需要更便宜、更好的电机，原始研究也值得研究](https://hackaday.com/2016/02/23/anti-cogging-algorithm-brings-out-the-best-in-your-hobby-brushless-motors/)。