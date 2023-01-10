# 一个很棒的开放式机械键盘

> 原文：<https://hackaday.com/2017/11/10/an-awesome-open-mechanical-keyboard/>

谁不想给自己的生活增加一点功能呢？感觉几个快捷键会让在 Eagle 中工作更顺畅一点，[dekuNukem]建立了自己的可编程机械键盘: [kbord](https://github.com/dekuNukem/kbord) 。

它具有不同动画的鲜艳 RGB LED 背光效果，15 个执行脚本的键——从 ctrl+c 到[后门](https://github.com/hak5darren/USB-Rubber-Ducky/wiki/Payload---OSX-Root-Backdoor)——或简单的按键，多达 32 个配置文件，以及一个小有机发光二极管屏幕来跟踪哪个键做什么！

kbord 使用 STM32F072C8T6 微控制器来控制成本、速度、引脚和外围设备，Gateron RGB 机械键——但任何带有 k bord led 开口的透明键和键帽都可以——在光漫射开关板上，SK6812 LEDs 用于光滑的美学。

休息之后，看看他的构建过程的延时视频之旅吧！(略带 NSFW、青春期幽默的几秒钟原本很酷的视频。这就是生活。)

 [https://www.youtube.com/embed/EGLLCtRuEuM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/EGLLCtRuEuM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[dekuNukem]必须运用一点小聪明来让 SK6812 LEDs 与 STM32 配合良好；他最终使用串行外设接口总线，并修补时序，以模仿 SK6812 所需的 800KHz 数据速率。最后的效果很值得。

定制键盘总是一项伟大的工程，无论是小的、[老式的](https://hackaday.com/2017/10/03/a-vintage-morse-key-turned-into-usb-keyboard/)、[被拆开重新利用的](https://hackaday.com/2017/09/18/sawed-off-keyboard/)，还是更大的。