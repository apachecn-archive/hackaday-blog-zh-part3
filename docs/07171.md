# 称重传感器告诉你不要吃油炸圈饼

> 原文：<https://hackaday.com/2017/09/21/load-cells-tell-you-to-lay-off-the-donuts/>

我们以前的代数老师常说，“你必须用你知道的去得到你不知道的。”这句话总是让我们想起传感器，它们将物理量转换成微控制器可以测量的东西。有时，项目的关键是了解哪种传感器将读取您感兴趣的系统的物理属性。如果物理特性是重量，您可以使用称重传感器。[DegrawSt]使用四个 50 千克的称重传感器，通过 Arduino 创建[浴室秤](http://www.instructables.com/id/Arduino-Bathroom-Scale-With-50-Kg-Load-Cells-and-H/)。

称重传感器通常包含变形时会改变电阻的应变仪。这实际上是测量力，但是如果你把它们装上，让它们测量你站在平台上所施加的力，你就得到一个秤。称重传感器通常有四个桥式应变仪。这会在电桥两端产生一个电压，尽管输出可能会有噪声，大约为毫伏级。

还有其他类型的称重传感器使用压电材料、液压、气动或其他技术。然而，应变计单元是最常见的。如果您想了解更多有关称重传感器的信息，请查看下面的[Rick Sellens]讲座。

为了给称重传感器提供激励并测量电压输出，通常需要使用放大器来调理电路。[DegrawSt]使用分线板上的 HX711 芯片来管理电池。Arduino 已经有了一个库，甚至还有一些示例代码。

四个测压元件允许 50 公斤的传感器读取一个人的体重，无论如何，高达 200 公斤。称重传感器本身采用桥式配置，将每个传感器的重量加在一起。

如果你想窥视商业规模的内部，我们以前见过。如果你不在乎看你的身材，也许你宁愿[拉紧你的带锯](https://hackaday.com/2017/01/28/bandsaw-tension-gauge-uses-raspberry-pi-and-load-cell/)。

 [https://www.youtube.com/embed/8G0HyW7rxWo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/8G0HyW7rxWo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

