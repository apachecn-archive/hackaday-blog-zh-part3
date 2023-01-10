# 两足动物鲍勃走路和跳舞

> 原文：<https://hackaday.com/2017/06/14/biped-bob-walks-and-dances/>

如果你有几个伺服电机、一个 Arduino 和一个蓝牙模块，你可以把制作[两足动物 Bob](https://circuitdigest.com/microcontroller-projects/arduino-bluetooth-biped-bob-robot) 作为一个周末项目。[B. Aswinth Raj]使用了 3D 打印机，但他也指出，你可以通过服务打印零件，或者只是从纸板上剪下它们。它们没那么复杂。

鲍勃的每条腿都有两个伺服电机:一个用于臀部，一个用于脚踝。当然，真正的工作在软件里，岗位把它一块一块分解。除了 Arduino 代码，还有一个使用 Processing 编写的 Android 应用程序。你可以自己构建，或者下载 APK。机器人通过蓝牙连接到手机，并提供一个简单的用户界面来做一些不同的行走步态和舞蹈。下面你可以看到两足动物 Bob 的一些视频。

对于一个年轻人或任何开始接触机器人的人来说，这将是一个不错的起步项目，尤其是如果你有一台 3D 打印机的话。然而，由于没有传感器，它相当有限。不过，如果你喜欢冒险，那也可以是第二版。

我们对蓝牙控制有着复杂的感情。蓝牙模块便宜且容易获得，但 ESP8266s 也是如此。将 Bob 放在 WiFi 上并让他为任何 web 浏览器提供自己的控制页面可能并不困难。

如果鲍勃遇到吉米，他会发现自己很羡慕。然而，吉米将是一个更具挑战性的建设。这些年来，我们实际上已经看到了不少[行走机器人](https://hackaday.com/2012/11/21/update-on-james-bipedal-robot/)。

 [https://www.youtube.com/embed/h3MPtHo1PvU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/h3MPtHo1PvU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/FT6tzJWxX_g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/FT6tzJWxX_g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

