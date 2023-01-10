# 快速 Arduino Hack 让无速度计的汽车显示换档点

> 原文：<https://hackaday.com/2016/11/28/quick-arduino-hack-lets-tach-less-car-display-shift-points/>

转速表曾经是只添加到最运动的汽车仪表板上的附件，但现在它们几乎是从时尚跑车到家庭卡车司机的所有东西的标准装备。如果你的日常司机天生没有转速表，不要担心——[一个简单的 Arduino 转速表](https://github.com/deepsyx/arduino-tachometer/)就在你的手边。

问题中的无转速表车辆是[deepsyx]的欧宝雅特，从下面的视频来看，它似乎有 pep 和手动变速器，这将使转速表特别有用。避开传统的模拟仪表显示，甚至数字读数，[deepsyx]选择用安装在一张旧信用卡上的四个 led 来指示换档点。第一个 LED 指示灯在转速为 4000 RPM 时亮起，随后的 LED 指示灯会在转速超过 500 RPM 时亮起。转速达到 5800 转/分时，所有指示灯闪烁，显示红线警告。[Deepsyx]甚至提供了平滑 RPM 值的串行输出，因此 RPM 数据的日志记录是未来可能的增强功能。

该项目使用线圈触发信号来感应发动机转速，这是一种从发动机控制单元(ECU)发出的信号，它告诉其中一个点火线圈点火。来自线圈组的高电压信号传递到火花塞，从而点燃气缸内的混合气。这是一个确定发动机转速的好方法，无需对汽车进行机械改造。只需确保您修改了代码，以获得车辆中正确的气缸数量。

简单、便宜、有效——即使它只是一个换挡点指示器，而不是真正的转速表，它也能完成工作。但是，如果你正在寻找一个更传统的显示器，并且有一辆更近的老爷车，[这个扫描 LED 转速表](https://hackaday.com/2014/07/07/visualize-vroom-with-this-rgb-led-tachometer/)可能更适合你。

 [https://www.youtube.com/embed/l8S7WWx-YB4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/l8S7WWx-YB4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[通过 [r/Arduino](https://www.reddit.com/r/arduino/comments/5edac1/i_made_a_car_tachometer_with_leds_and_arduino/)