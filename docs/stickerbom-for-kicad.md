# KiCad 的贴纸

> 原文：<https://hackaday.com/2016/02/09/stickerbom-for-kicad/>

当电路板较大且元件大多通过孔时，设计师可以在 silk legend 上放置大量信息——参考指示符、值、附加文本等等。但是，随着表面贴装元件变得越来越小，电路板的面积越来越大，现代电路板的丝绸层上没有很多信息。如果您正在构建和发布一个短期的工具包，也许是为了一轮 beta 测试，那么[Adam Greig]的用于 KiCad 的[sticker BOM python 脚本会非常方便。StickerBOM 是一个 KiCad BOM exporter，专为手工填充纸板的人设计。它为可打印的粘性标签生成 PDF，其中每个标签反映供应商的一个 BOM 行。然后你把这些标签贴在供应商的包上，它们会告诉你零件的去向。](https://github.com/adamgreig/agg-kicad/wiki/StickerBOM)

标签印有参考指示符、数量、组件价值、包装、供应商和零件号。它还添加了 PCB 图，突出显示了相关器件，以便于识别位置。要使用它，原理图符号必须添加供应商字段和零件号。该脚本可以从命令行运行，也可以从 eeschema 中的 BOM 管理器运行。该脚本是为 Avery L7164 标签设置的，但此设置可以更改。这项工作仍在进行中，所以需要注意一些问题。它不能处理纸板的底层，结果只和你提供的数据一样好。如果你有一个大电路板，上面散布着各种元件，那么印在标签上的图形可能就不理想了。

我们希望这一点，以及其他脚本，如[零件生成器和成本电子表格](http://hackaday.com/2015/12/05/kicad-utilities-generate-parts-track-costs/)或用于机械 CAD 导出的[脚本](http://hackaday.com/2015/11/08/kicad-script-hack-for-better-mechanical-cad-export/)，能够添加到 KiCad 的未来版本中。 [KiCad 第 5 版开发者路线图文档](https://kicad.readthedocs.io/en/latest/Documentation/development/road-map-r5/)已经有了一些非常好的新特性。