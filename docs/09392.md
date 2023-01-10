# 一个开源的接线图工具

> 原文：<https://hackaday.com/2018/05/09/qelectrotech-an-open-source-wiring-diagram-tool/>

有一些开源选项可以用来创建电气原理图。KiCad 和 [Fritzing](https://hackaday.com/tag/Fritzing/) 将带您从原理图捕捉到 PCB 布局。然而，创建接线图的选择有限。通常这些是在微软的 Visio 中创建的，它既不是开源的，也不太适合这项任务。

ElectroTech 是一个用于绘制这类图表的开源工具。它由两个工具组成:用于创建原理图符号的元素编辑器和用于创建图形的原理图编辑器。通用符号库也包括在内，以及[T4【IEC 60617】标准化符号。](http://std.iec.ch/iec60617)

作为一个原理图编辑器，QElectroTech 在绘制组件之间的清晰连接方面做得很好。连接以 90 度角自动布线，易于拖动。不仅仅由电气连接组成的系统也非常适合该软件。在这里，您可以看到管道和手动阀以及电子传感器和执行器都在同一张图中。

下次你需要记录一些东西的连线时，QElectroTech 是一个不错的选择。它从 2008 年就开始了，目前正在积极开发中，有 Windows、OSX 和 Linux 版本(包括一个用于夜间构建的 PPA)。