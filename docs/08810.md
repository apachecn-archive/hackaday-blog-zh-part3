# Autodesk 引入了参数化零件生成

> 原文：<https://hackaday.com/2018/03/08/autodesk-introduces-parametric-part-generation/>

任何 PCB 设计中最困难的部分是添加器件和元件。你不应该使用随机零件库，创建自己的零件库只是一种痛苦。为什么我们要忍受这种痛苦这么久，尤其是考虑到大多数组件都遵循一个标准？此外，在机械 CAD 工具中进行 3D 建模和绘制电路板现在已经成为一件事情，这使得创建自己的零件库变得更加复杂。

为了解决这个问题， [Autodesk 推出了 library.io](https://library.io/) ，这是一个为 Eagle 参数化生成组件封装图和为 Fusion360 生成 3D 模型的工具。鉴于大多数零件都遵循一个标准——QFP、TO、DFN 或 sot 23——这是现在在 Eagle 中创建新零件的最简单方法，它具有自己的 3D 模型，允许您将其引入机械 CAD 工具。

Autodesk 论坛上有一篇关于参数化零件生成的概述[，介绍了这一新工具的功能。实际上有两个不同的版本，一个是基于网络的应用程序，允许您在浏览器中参数化地创建封装和封装，并将它们导出为库。该工具的另一个版本与 Eagle 集成在一起，允许您在 Eagle 中创建一个新的参数化组件。](https://forums.autodesk.com/t5/eagle-forum/eagle-8-7-parametric-2d-amp-3d-model-generation-library-io-more/td-p/7836642)

这与创建新足迹的标准方法相去甚远。创建一个新的参数封装就像复制几个数字一样简单，而不是埋头于数据手册，将尺寸合适的焊盘放到网格上。除了新的参数化设计功能之外，Eagle 中还有一个新工具，它不再需要为符号放置和命名管脚。现在，您只需从数据手册中剪切并粘贴引脚列表。

需要注意的是，用 library.io 工具创建的所有东西都可以下载并离线使用。结合最近的新闻 [KiCad 现在可以接收 Eagle 板和原理图文件](https://hackaday.com/2018/02/10/whats-coming-in-kicad-version-5/)，你也有办法在每个人都喜欢的开源 PCB 工具中创建参数足迹。