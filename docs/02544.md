# 廉价扭矩传感器回归应变计的基础

> 原文：<https://hackaday.com/2016/06/20/cheap-torque-sensor-goes-back-to-basics-on-strain-gauges/>

迟早，我们都要处理扭矩测量的问题。我们大多数人永远不需要超越千分尺式扭矩扳手发出的令人满意的咔哒声，或是松开离合器时无绳电钻的刺耳嗡嗡声。但在某些时候，你可能真的需要测量扭矩，在这种情况下，这本扭矩传感器指南可能正是你需要的。

[Taylor Schweizer]关于扭矩的四部分系列相当全面。上面的链接是他的 DIY 扭矩传感器的实际构建，但前三部分也非常值得一读。[Taylor]将自己描述为电子垃圾鉴赏家，并向我们展示了他的产品可能是用回收的零件制成的，但最终一个 20 美元的应变仪包和一个 LM358 是他验证概念的最快方式。应变仪被超级粘在一个插座上，热胶被大量地用于绝缘和应变消除，整个东西被连接到一个小盒子上用于数据采集。一个快速脚本和数据转储到 Excel，你就有了一个可视化扭矩的方法。

用于实时测量的 LCD 显示器正在工作中，对仪表放大器的改进也在工作中——对此[泰勒]可能想参考[【比尔·赫德】的](http://hackaday.com/2015/03/16/instrumentation-amplifiers-and-how-to-measure-miniscule-change/)或[【布兰登·邓森】关于这个主题的](http://hackaday.com/2016/03/18/beyond-measure-instrumentation-amplifiers/)最近的帖子。

[通过 [r/arduino](https://www.reddit.com/r/arduino/comments/4lmb8z/i_made_a_cheap_torque_sensor_with_a_socket/)