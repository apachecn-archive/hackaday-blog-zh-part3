# 开源激光切割机软件获得重大更新，新功能

> 原文：<https://hackaday.com/2016/07/17/open-source-laser-cutter-software-gets-major-update-new-features/>

LaserWeb 项目最近发布了第 3 版，有许多新功能和改进，准备给你的激光切割机或雕刻机一个大的能力提升！最重要的是，新的 3 轴 CNC 支持意味着 LaserWeb 可以为其他 CNC 工具做它已经为激光切割和雕刻做的事情。

LaserWeb3 支持不同的控制器和它们可能连接的机器——无论是自制系统、配备激光二极管发射器的 CNC 框架(如改装的 3D 打印机),还是那些负担得起的蓝盒 40W 中国激光器，其专有控制器被类似[光滑滑板](http://smoothieware.org/smoothieboard)的东西取代。

我们在过去已经[报道过 LaserWeb 项目，但是从那以后**已经贡献了一整批**新的开发，带来了更好的性能和新的功能(比如 CNC 模式)和新的用户界面。最新版本不仅改进了将多个文件和格式导入单个多层作业的能力，还提供了 Smoothieware 软件以太网支持和作业成本估算器。LaserWeb3 中的性能目前在 Smoothieware 中是最好的，但您仍然可以保存和导出 GCODE，以便在 Grbl、Marlin、EMC2 或 Mach3 中使用。](http://hackaday.com/2016/01/26/stop-driving-laser-cutters-with-3d-printer-software/)

这个项目向 CNC / Javascript / UX 开发者开放，让它更上一层楼。如果您有兴趣帮助进一步推进该项目，并帮助它为 3 轴 CNC 做它为激光切割所做的事情，项目协调员[Peter van der Walt]希望您前往[github 知识库](https://github.com/openhardwarecoza/LaserWeb3)！

我们最近分享了许多关于[安全自制激光切割机设计](http://hackaday.com/2016/06/29/taming-the-beast-pro-tips-for-designing-a-safe-homebrew-laser-cutter/)的重要信息。你是自己做激光切割机，还是改装现有的？请在评论中告诉我们吧！