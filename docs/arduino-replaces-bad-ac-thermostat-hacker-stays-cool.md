# Arduino 替换坏的交流恒温器，黑客保持冷静

> 原文：<https://hackaday.com/2016/08/05/arduino-replaces-bad-ac-thermostat-hacker-stays-cool/>

过去两周，北美大部分地区一直处于创纪录的热浪中，廉价的窗式空调设备正从当地的大型商店中飞出。然而，并非所有这些打折商品在横渡太平洋之前都经过严格的质量控制，一些不可靠的恒温器肯定会通过。但是只要付出一点汗水，你就可以用这个 Arduino 恒温器和温度显示器来修理它。

我们将规定 Arduino 对于这个应用来说可能是多余的，并且微控制器不属于每个项目。但是如果这是你手头的东西，并且你厌倦了在一滩汗中醒来，那么这是一个完全可以接受的解决方案。看起来像是[工程废话]运气好，有一个带低电流电源开关的单元，允许他使用一个小继电器来控制交流电。控制算法非常简单——接受来自编码器的设定值，读取温度传感器，并相应地打开或关闭空调。设定值和当前温度显示在有机发光二极管屏幕上。我们建议的一个改进是在电源周期之间增加三分钟的延迟，就像交流状态的面板一样。

这个项目与 Arduino 控制的 AC 有一些相似之处，但对我们来说似乎更粗糙。这是一件好事——黑客必须以某种方式保持冷静。

 [https://www.youtube.com/embed/da1wP5CTxi4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/da1wP5CTxi4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

