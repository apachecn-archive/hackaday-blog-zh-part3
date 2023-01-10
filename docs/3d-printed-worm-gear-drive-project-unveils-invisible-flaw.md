# 本周失败:3D 打印蜗轮传动项目揭露隐形缺陷

> 原文：<https://hackaday.com/2018/05/11/3d-printed-worm-gear-drive-project-unveils-invisible-flaw/>

我们所有人都希望在花费更少资金的情况下将我们的项目付诸实施。有时候我们的抄底会有回报，有时候不会。我们中的许多人对失败只是耸耸肩，然后继续前进，但这不是(马克·里霍斯特)的风格。他试图围绕一个来自全球速卖通的廉价蜗轮为他的 3D 打印机制造一个 Z 轴驱动器。这个项目注定会被一个肉眼看不见的齿轮缺陷所破坏，但是他[记录了这个经历](https://drmrehorst.blogspot.com/2018/04/designing-low-cost-printable-worm-gear.html)，所以我们都可以跟着做。

我们之前已经介绍过[Mark]的不断发展的打印机项目，因为我们喜欢阅读他的详细记录的升级冒险。他不羞于探索违背 3D 打印机惯例的想法，从使用[皮带驱动 Z 轴](https://hackaday.com/2018/01/04/huge-3d-printer-ditches-lead-screw-for-belt-driven-z-axis/)到[将打印冷却风扇从打印头上移开](https://hackaday.com/2018/02/06/cpap-hacked-into-super-charged-3d-printer-cooler/)(随后还有[的](https://hackaday.com/2018/04/29/hard-drive-gives-its-life-to-cool-3d-prints/))。幸运的是，他并不羞于在成功的同时记录他的失败。

他向我们介绍了这个项目，从最初的动机开始，到零件选择，并描述了他如何设计他的变速箱零件来克服 3D 打印固有的缺点。齿轮箱安装后，产生的打印出来有缺陷。 [![](img/2e32d3cb7dc1af664cc26448bd768461.png)](https://hackaday.com/wp-content/uploads/2018/06/mrehorst-2mm-error.jpg) 每一个有规律间隔的印刷凸起都可以直接与蜗轮的一次转动相关联，这使其成为首要怀疑对象。然后，为了更严格地验证这一观察结果，用指示器测量 Z 轴运动，并相对于期望的运动作图。如果问题是由一块碎片或表面损坏引起的，那将在图中产生一个急剧的凸起。正弦曲线告诉我们问题比这更根本。

这种特殊的蜗轮通过增加电机扭矩提供了足够的提升力来移动打印床，但它也增加了缺陷，使其不适合精确定位 3D 打印机的 Z 轴。[Mark]计划在他找到更好的蜗轮源时重新考虑这个想法，当他找到时，我们肯定会有机会看到会发生什么。