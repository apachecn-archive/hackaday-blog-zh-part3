# 还记得白手起家的机器人有多难吗？

> 原文：<https://hackaday.com/2018/01/02/remember-when-scratch-built-robots-were-hard/>

过去，即使是简单的机器人也需要相当大的努力才能组装起来。这个例子显示了我们在使用工具和技术使事物移动和交互方面取得了多大的进步。这是由手机触摸屏控制的 3D 打印漫游车。这实现了轮式机器人最基本的构建模块，这个过程对你和你的钱包来说都很容易。

我们无法停止对这些项目的热爱。我们刚刚看到[他的气动飞机引擎](https://hackaday.com/?p=286769)，现在这个小漫游车竖起我们的耳朵。该设计使用了两个带滚珠轴承的动力轮这一熟悉的技巧，以避免差速转弯的问题。但是简单都在实现中。

这个机器人是 3D 打印的，使用了八个非常简单的部件:四个齿轮，两个轴，一个盖子和一个托盘来安装所有东西。盖子抓住滚珠轴承，滚珠轴承在托盘底部戳出一个孔，形成一个全向轮。两个 9G 伺服系统为连续旋转而改进。齿轮的啮合齿位于轮段上，轮段上有氯丁橡胶 O 形圈凹槽，以提供牵引力。整件事都是由一台 ESP8266 以 Adafruit Feather Huzzah 的形式驱动的。这是使用 Arduino IDE 编程的，您的手机可以直接连接或通过 WiFi 路由器连接。

我们没疯，对吧？机器人以前不是这么容易组装的吗？这是因为 3D 打印相对于传统基底制造方法的强大，但在于强大而廉价的嵌入式系统的可用性以及对它们进行编程的可用工具和库。你[Greg]向我们展示了当前可用的构建模块在任何想要引导他们的工程创造力的人手中是多么伟大，这是值得称赞的。他当然有… [这个底盘最终为圣诞老人的雪橇提供动力](http://www.instructables.com/id/Santa-Sleigh-Wifi-Edition/)。

需要更大的印刷挑战？这是一辆 3D 打印的漫游者，[配备了悬挂系统](https://hackaday.com/2017/06/24/3d-printed-rover-rolls-light-and-looks-right/)。

 [https://www.youtube.com/embed/qshOzd6yuKc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/qshOzd6yuKc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[途径 [Adafruit](https://blog.adafruit.com/2017/12/26/motorized-wifi-controlled-chassis/)