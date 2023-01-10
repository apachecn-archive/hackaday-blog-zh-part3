# 索诺夫之子

> 原文：<https://hackaday.com/2017/05/12/son-of-sonoff/>

我们已经报道过几次 Sonoff——一个非常便宜的盒子，里面有一个 ESP8266、一个电源、一个交流继电器以及一个接入电源线的方法。非常便宜是指 5 美元或 6 美元。提供的软件将与几个系统(包括最近的 Alexa)一起工作。但是哪个有自尊的黑客会想在内置 ESP8266 的东西上运行股票固件呢？

当然没有。但他也知道，他不想每次想要部署交换机时都要从头开始。所以他构建了[sonofboilerplate](https://tzapu.com/sonoff-firmware-boilerplate-tutorial/)并将代码放在 [GitHub](https://github.com/tzapu/SonoffBoilerplate) 上。该代码使用 web 门户管理配置(包括网络设置),可以通过无线方式更新自身，并与 Blynk 和 MQTT 集成。如果你不喜欢那个代码库，还有[其他选择](https://github.com/arendst/Sonoff-MQTT-OTA-Arduino)，包括一个有故障安全[重新配置模式](https://github.com/arendst/Sonoff-Tasmota)。

你必须将一个接头焊接到电路板上才能重新刷机。因为所有这些都提供了空中更新，如果你愿意，你可以按下标题来获得初始的 flash。

当然，如果你愿意，你也可以完全重新编程。或者使用股票固件，像所有正常人一样控制它。

如果您计划使用 Blynk，我们之前已经讨论过了。就此而言，我们也讨论过 [MQTT](https://hackaday.com/2016/06/02/minimal-mqtt-power-and-privacy/) 。在下面的视频中，你可以看到更多关于 Sonoff 的细节，包括内部的快速展示。

 [https://www.youtube.com/embed/mX97u_pQYnU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/mX97u_pQYnU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

