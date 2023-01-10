# 将 Eagle 库导出到 FOSS 工具

> 原文：<https://hackaday.com/2017/12/21/exporting-eagle-libraries-to-foss-tools/>

自从 Autodesk 收购后，Eagle 一直在社区中兴风作浪。开放式硬件 PCB 设计的*事实上的*标准现在正在采用推拉式布线，一个将电路板翻转到背面的按钮(天才！)，与 Fusion360 的集成，组件的自动化 3D 渲染，以及一堆其他简洁的工具。然而，Eagle 也不是没有缺点，人们希望将无数的 Eagle 电路板布局和库移植到其他 PCB 设计包中。[这个工具就是做这个的](http://vk5hse.blogspot.com.au/2017/12/importing-cadsoft-eagle-binary-layouts.html)。

该工具是用于电路板编辑的 FOSS 工具 [pcb-rnd](http://repo.hu/projects/pcb-rnd/) 的扩展，此次更新大规模扩展了对 Eagle 板和库的支持。举个例子，[VK5HSE]装了一只鹰。收发器的 brd 文件，选择管脚头，并将该元件导出到 KiCad 库。第一次成功了。另一个实验，曾经流行的电视-B-消失了。brd 文件直接导出到 pcb-rnd。这是 Eagle to KiCad、Eagle to Autotrax 和 Eagle to gEDA PCB 的一个基本完整的解决方案，只有一些与铜浇注和丝网印刷相关的最小警告，如果您不是盲目地使用该工具，没有什么是不能处理的。

必须指出的是，大多数开放硬件项目适合 80 cm ² 板区域，因此可以使用 Autodesk 的 Eagle 的*免费使用版本*打开和修改，这是一个非常强大的工具，可以将 Eagle 板和库转化为可以使用 FOSS 工具构建的设计。

谢谢[Erich]的提示。