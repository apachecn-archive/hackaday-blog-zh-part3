# KiCad 脚本黑客更好的机械 Cad 输出

> 原文：<https://hackaday.com/2015/11/08/kicad-script-hack-for-better-mechanical-cad-export/>

开源 EDA 软件 KiCad 最近获得了很大的吸引力。CERN 一直在投入资源引入许多新的高级功能，如差分对轨道、推推式路由以及更多计划中的功能。EDA 软件包的一个重要要求是通过以行业通用格式导出 3D 模型来实现与机械 CAD 软件包的无缝接口。这改善了协作，并允许进一步的工程设计，如生产外壳和面板。

KiCad 很久以前就有 3D 浏览器了。但是它使用 VRML 网格格式(。wrl 文件)并且存在兼容性问题，这使得它无法渲染某些版本的 VRML 文件。此外，VRML 网格导出不是特别有用，因为它在机械 CAD 软件中不容易操作。KiCad 的最新版本现在提供 IDFv3 格式导出–中间数据格式，这是一种用于设计和分析印刷布线组件的机械数据交换规范。利用这一新功能，[Maurice]创建了 [KiCad StepUp](https://hackaday.io/project/7926-kicad-stepup-script-hacks-mcad-world) ，这是一个允许 KiCad 和 FreeCAD 之间协作交换的导出脚本。

FreeCAD 宏和相应的配置文件被添加到 KiCad 项目文件夹中。你从。用于 KiCad 设计中使用的所有组件的 STEP 文件。下一步是转换并保存所有。STEP 文件为。使用 FreeCAD 的 WRL 格式。在 KiCad 方面，您使用。WRL 像往常一样归档。当您想要导出电路板时，使用 KiCad 中的 [IDFv3](https://www.simplifiedsolutionsinc.cimg/idf_v30_spec.pdf) 选项。当[Maurice]的 StepUp 脚本运行时(在 KiCad 之外)，它会替换的所有实例。WRL 的档案中有相应的资料。STEP 将电路板和组件版本化并导入 FreeCAD。STEP 型号。结果是一个板及其填充的组件，可以作为常规的三维对象进行操作。

首先，从 Sourceforge 资源库下载[升级源代码](http://sourceforge.net/projects/kicadstepup/)。[Maurice]还利用 FreeCAD 的参数化功能建立了一个大型的 3D 模型库[,包括。一步并。每个组件的 WRL 模型。如果您需要额外的资源，请查看在线服务，如](https://github.com/easyw/kicad-3d-models-in-freecad/) [GrabCAD](https://grabcad.com/) 和 [3DContentCentral](http://www.3dcontentcentral.com/) ，在那里您可以获得。几乎所有常用组件的 STEP 模型。该升级下载包含一个演示项目和用户指南，可帮助您入门。[Maurice]还包括另一个 FreeCAD 宏来帮助缩放、移动和旋转模型。

脚本配置文件允许您设置 3D 模型文件夹的路径，并为 PCB 指定颜色。也可以忽略某些类别的组件(如最小的组件或对机械布局不重要的组件)导入 FreeCAD。这有助于减少加载时间和文件大小。我们尝试了一下这个新的脚本和工作流程，在经历了一些挫折之后，我们成功地完成了转移。如果您有任何反馈，[Maurice]很乐意在 [kicad.info 论坛](https://forum.kicad.info/t/kicad-stepup-new-exporter-for-3d-mcad-feedbacks-are-welcome/1048)上听听您的意见。该论坛也将是一个很好的地方，要求任何帮助，你需要与 KiCad 升级。

第一个视频展示了 StepUp 脚本的安装和使用，第二个视频演示了如何将 CrazyFlie 四轴飞行器从 KiCad 导出到 FreeCAD。

 [https://www.youtube.com/embed/Ukd47VXYzQU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Ukd47VXYzQU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/XmNGdqkKbpM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/XmNGdqkKbpM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

