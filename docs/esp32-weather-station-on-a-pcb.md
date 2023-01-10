# PCB 上的 ESP32 气象站

> 原文：<https://hackaday.com/2018/02/10/esp32-weather-station-on-a-pcb/>

我们看到许多 ESP8266 项目，但 ESP32 项目却少得多。所以这个使用 ESP32 的 PCB 上好看的[气象站吸引了我们的眼球。该板有几个用于普通天气设备的插座，但稍加修改，它将成为 ESP32 的一个伟大载体。由于 PCB 布局是可用的，你可以改变周围的东西来适应你。你可以在下面的视频中看到[Rui Santos]关于他的项目及其从试验板到 PCB 的进展的视频。](https://randomnerdtutorials.com/build-an-all-in-one-esp32-weather-station-shield/)

假设您构建的电路板没有任何变化，您有空间:

*   2 个 SMD LEDs
*   1 个按钮
*   1 个微调按钮
*   1 个 DHT22 温度和湿度传感器
*   1 个 BMP180 气压传感器
*   1 个光敏电阻
*   1 个 MicroSD 卡模块
*   2 个输入/输出端子板

使用的 ESP32 [Rui]本身就是一个模块。ESP32 DOIT DEVKIT V1 板看起来像 IC 封装。如果您对它进行套接字处理，您可以很容易地为以后的其他项目移除该模块。

ESP32 代码提供了一个 web 服务器来显示其测量值。该页面使用 AJAX，它允许服务器在不刷新页面的情况下更新页面上的值。

如果你宁愿[控制世界](https://hackaday.com/2018/01/11/esp32-makes-not-so-smart-lights-smart/)而不是监视它，你也可以这样做。如果你想过分，你可以用不少于五个 esp 32 来建造[时钟。](https://hackaday.com/2017/11/27/over-engineered-clock-uses-no-less-than-five-esp32s/)

 [https://www.youtube.com/embed/m5cS21AAhZo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/m5cS21AAhZo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

