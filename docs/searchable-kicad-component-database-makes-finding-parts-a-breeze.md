# 可搜索的 KiCad 组件数据库使查找零件变得轻而易举

> 原文：<https://hackaday.com/2018/06/17/searchable-kicad-component-database-makes-finding-parts-a-breeze/>

开源 EDA 软件 KiCad 受到黑客读者和整个硬件社区的欢迎。但是它也不能免受 EDA 工具最常见的危害。管理您的符号库和封装外形库，并为您最新设计中使用的组件找到新的符号库和封装外形库，很少会是一种愉快的体验。为了帮助减轻你的痛苦，[twitchyliquid64]创建了 [KiCad 数据库(KCDB)](https://kcdb.ciphersink.net/) 。一个非常简单的 web 应用程序，用于搜索元件足迹。

该数据库使您可以通过可选参数(如引脚数)轻松搜索封装外形名称。当然，它也可以通过标签进行搜索，以获得一点灵活性(搜索 Neopixel 返回如上所示的足迹)。还有一个 Kicad 官方零件的指标，这是一个很好的接触。 我们最喜欢的功能之一是零件查看器，它可以在浏览器中显示轮廓，让您很容易立即看到零件是否合适。AngularJS 和材料设计在这里工作，[主应用程序是用 Go](https://github.com/twitchyliquid64/kcdb) 写的——非常新潮。

该数据库由[twitchyliquid64]公开托管，但可以很容易地在您的机器上本地运行，您可以在那里添加自己的库。只需一个命令就可以添加一个 GitHub repo 作为组件源，然后定期“摄取”它。添加一个你曾经发现的整洁的脚印库，然后忘记它们，安全地知道它们将来可以很容易地在和其他东西一样的地方被发现，这是多么容易啊。

如果您找不到您正在使用的零件的原理图符号，我们最近报道了一项[服务，它使用 OCR 和计算机视觉从数据表](https://hackaday.com/2018/06/12/computer-vision-for-pcb-layout/)中自动生成符号；很酷的东西。