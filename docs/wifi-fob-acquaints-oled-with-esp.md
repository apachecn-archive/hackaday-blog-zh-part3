# WiFi 离岸价让有机发光二极管了解 ESP

> 原文：<https://hackaday.com/2015/10/16/wifi-fob-acquaints-oled-with-esp/>

当你想到项目中的 WiFi 时，很容易陷入这样一个常规，即假设目标是为某些东西添加 WiFi。这种特殊的构建实际上为你带来了 WiFi 意识，通过嗅探[你周围的信号](https://hackaday.io/project/7990-microusb-powered-esp8266-oled-board)并显示它们以获得即时反馈。

[ [0miker0](https://hackaday.io/hacker/11361) ]正在做这个项目，作为他在[方寸项目](https://hackaday.io/project/7813-the-square-inch-project)的参赛作品。它是一种适配器板，具有用于 ESP8266-01 模块的 2×4 引脚接头的尺寸，并承载 128×64 有机发光二极管显示器的元件和焊盘。这些变得相当普遍，不难找出原因。它们相对便宜、低功耗、高对比度，并且需要很少的支持元件。从[GitHub Repo](https://github.com/mike-rankin/ESP8266_OLED_Display)的原理图来看，它看起来像 5 个电阻和 7 个电容。

下面的视频展示了迄今为止的两种固件模式。第一个是读取一些信息的 AP 扫描，第二个是天气显示程序。任何使用过 ESP 模块的人都知道，他们有可能收集关于 WiFi 信号的各种数据——我们最喜欢的演示之一是[cnlohr]用它来创建他的 WiFi 信号强度的 3d 光绘图[。在这个东西上放一个可充电的吸脂器，根据你的需要调整示例代码，你就有了一个新的用于驾驶的小工具。](http://hackaday.com/2015/02/17/mapping-wifi-signals-in-3-dimensions/)

 [https://www.youtube.com/embed/o5fJGXnqNC0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/o5fJGXnqNC0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



看起来这个月早些时候我们[提到的方寸项目](http://hackaday.com/2015/10/02/the-square-inch-project-challenges-your-layout-skills/)已经有了 29 个参赛作品。你还有时间开始你的设计……把它加入到这个周末的黑客列表中。