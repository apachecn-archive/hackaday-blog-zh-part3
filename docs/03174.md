# 星轨:激光定位天文学的一课

> 原文：<https://hackaday.com/2016/08/10/star-track-a-lesson-in-positional-astronomy-with-lasers/>

当我们开始阅读他在 Arduino 供电的星星指针上的教程时，他用定位天文学的教程威胁我们，他做到了。我们会选他帮我们把魔戒带到魔多。我们永远不会迷路，他的威胁传递率使他不太可能拉博罗米尔。

正如我们所提到的，他从一本非常简洁、写得很好的天球坐标教程开始，这是古代人非常想拥有的。如果我们要写一点代码来做我们自己的定位天文系统，这是我们要打开的标签。顺便说一句，这正是他鼓励那些跟随教程的人去做的。

星星指针本身是一个高功率的绿色激光指针(电池供电)，3D 打印部件，以及 14 美元的中国科技产品的混合物。该项目使用两个 Arduino 克隆来处理串行命令并管理两个 [28byj-48](http://hackaday.com/2016/05/02/simple-robot-arm-with-steppers-has-pleasingly-smooth-motion/) 步进电机。第二个 Arduino 克隆纯粹是为了补充第一个的数字引脚；我们对此停顿了一下，但后来我们意识到，进口 arduinos 已经变得如此便宜，它们可能比 I2C 分线板或步进驱动器更实惠。机体的设计混合了 Tinkercad 和一些我们没听说过的东西， [OpenJsCAD。](http://joostn.github.io/OpenJsCad/)

一旦组装好并测试完毕，剩下唯一要做的事情就是带着你的新发明出去。在确保你已经遵守了当地所有关于不要将激光对准飞机的规定后，将激光对准北极星。之后，你可以插入任何一个恒星坐标，激光就会向它摆动，并跟踪它在天空中的位置。相当酷。

[https://player.vimeo.com/video/176745067](https://player.vimeo.com/video/176745067)