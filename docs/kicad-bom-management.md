# KiCAD BOM 管理

> 原文：<https://hackaday.com/2016/03/16/kicad-bom-management/>

KiCAD 仍然是设计 PCB 和其他电路的流行工具，这是有充分理由的:它功能多样，几乎拥有构建任何类型电路板所需的一切。不过，这也伴随着一个相当陡峭的学习曲线，而且[Jeff]对 KiCAD 中的物料清单(BOM)特性特别失望。在应用了一些 Python 和 Kivy 之后，[Jeff]现在有了一个 [BOM manager，弥补了 KiCAD 的一些不足](https://github.com/Jeff-Ciesielski/Boms-Away)。

目前，该工具处理原理图导入、相似元件合并和用户管理的零件数据库，可用于存储和检索将来常用的零件。所有更改都可以保存回原始原理图。[Jeff]希望他的工具能为那些一年生产多块 PCB 并且不得不处理 KiCAD 缺乏 BOM 特性的人节省一些时间。

[Jeff]仍然有一些他想添加的特性，比如单元测试、用户指南和更简洁的用户界面。你还希望 KiCAD 增加哪些功能？

这个脚本对任何有类似挫折的人来说都是一个很好的工具。KiCAD 的修改和扩展也很受欢迎:已经有了用于机械 CAD 导出的工具，部件生成器和成本跟踪工具，以及从 T4 的 Eagle 到 KiCAD 的转换器。