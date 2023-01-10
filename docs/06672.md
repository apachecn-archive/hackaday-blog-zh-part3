# 使用逻辑分析仪生成游戏男孩的截图

> 原文：<https://hackaday.com/2017/08/01/using-a-logic-analyzer-to-generate-screenshots-from-a-game-boy/>

难道你不想回到一个死亡的掌上电脑，提取你的 90 年代高分的证据吗？你当然会。

[![](img/862bf3ee00ecd6aad40a689b0d43a8ec.png)](https://hackaday.com/wp-content/uploads/2017/07/mole-mania.png)【svendahlstrand】从 Saleae 买了他的第一台逻辑分析仪，一台 Logic 8，并决定和一个老游戏男孩一起玩。他用三点螺丝刀打开手持设备，将六根电线连接到 LCD 数据总线上，根据记录的数据生成屏幕截图。他得到了《所罗门俱乐部》、《鼹鼠狂热》、《德拉库拉小孩》等电影的屏幕。

最初的几次尝试充满了不幸，因为[斯文]试图弄清楚他的新分析仪的设置。在一个例子中，他反转了数据 0 和数据 1 信号，也反转了两个灰度值。弄清楚之后，他把自己的 [LCD 嗅探教程](https://github.com/svendahlstrand/game-boy-lcd-sniffing)贴到了 GitHub 上，在 GitHub 上他还有一个 C 程序，可以手动一个像素一个像素地拼接屏幕截图。

感谢[sven]将这个项目发布到我们最近的[上，你需要知道的关于 Logic Probes 的一切都发布在](http://hackaday.com/2017/07/29/everything-you-need-to-know-about-logic-probes)上。