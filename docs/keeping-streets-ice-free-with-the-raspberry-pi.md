# 用覆盆子酱保持街道不结冰

> 原文：<https://hackaday.com/2018/04/17/keeping-streets-ice-free-with-the-raspberry-pi/>

[Revanth Kailashnath]来信告诉我们他和他的团队正在为格拉斯哥大学的“实时嵌入式编程”课程进行的一个有趣的项目。为了应对格拉斯哥严酷而危险的冬天，他们的系统使用树莓皮和一套传感器来自动向街道和人行道部署盐水溶液。虽然该项目仍然只是一个概念验证，尚未部署，但该团队迄今为止所做的工作涵盖了从开发自己的 PCB 到创建基于网络的用户界面的所有领域。

[![](img/618c11251269268870907a0f18f64fd8.png)](https://hackaday.com/wp-content/uploads/2018/04/icepi_detail.png) 核心思想很简单。如果条件适合结冰，喷洒盐水。使用盐水是一种既便宜又安全的清除和防止结冰的方法，因为它只是降低了水结冰时的温度(T4)。最终结果是，冰不会形成，直到它下降到 10 华氏度(-12 摄氏度)左右。不是一个完美的解决方案，但它肯定会有所帮助。当然，你不会想在人们经过的时候用盐水喷他们，所以事情远不止如此。

使用古老的 DHT22 传感器，团队可以获得当前的温度和湿度，这使他们能够确定何时开始喷洒。但为了防止任何潮湿和愤怒的行人，使用了 HC-SR501 PIR 运动传感器。如果系统看到运动，它会停止一段时间，让活动安静下来。

监控传感器和控制泵是由一个用 C++编写的守护程序完成的，这个守护程序还将数据记录到一个 SQL 数据库中，这个数据库反过来又提供给它们的 PHP web 接口。在休息后的视频中，[Revanth]展示了系统如何根据各种传感器的输入不断做出决策。每隔几秒钟分析一次环境数据和运动，以提供实时解决方案。

我们已经报道了几个旨在通过加热混凝土来融化冰雪的项目，但有趣的是看到了一种解决这种常见冬季烦恼的“智能”方法。

 [https://www.youtube.com/embed/QaHXD64GoVk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/QaHXD64GoVk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

