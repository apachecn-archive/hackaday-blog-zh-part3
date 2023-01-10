# 1 BTN–开源 Dash

> 原文：<https://hackaday.com/2016/04/29/1btn-an-open-source-dash/>

廉价收音机、无处不在的 WiFi 和强大的网络服务的出现意味着物联网浪潮将会持续下去。亚马逊通过它的“只做一件事”破折号按钮加入了进来。但一个更有趣的解决方案是一个物联网“全部完成”按钮。

【Anand】致力于他的 [1btn 开源 WiFi 连接物联网按钮](https://hackaday.io/project/11269-1btn-open-source-wifi-connected-iot-button)已经有一段时间了。它通过 WiFi 连接到互联网，使用简单的在线界面触发您分配给它的任何操作。它是可重构和开源的。这意味着它可以以非常富有想象力的方式使用，如果需要，如果你决定真正使用它，可以用你自己的定制固件重新刷新。

1btn 的 ESP8266 模块通常处于睡眠模式，当按下按钮时唤醒，建立连接，执行任务，然后在收到确认后返回睡眠状态。红色/绿色 LED 指示操作是否成功。你可以设置它通过自定义脚本、API 或 if TTT-maker 通道发送电子邮件、消息、推文或执行操作。为了方便黑客，所有的 ESP8266 GPIO 引脚都可以通过接头访问。例如，这便于添加外部传感器。还有一个(未填充的)QFN 足迹，允许添加 ATmega 设备(168P/328P ),其 GPIO 引脚也可通过接头访问。这为该设备开辟了大量的附加应用，例如家庭自动化。

在软件方面，1btn 连接到一个[网络控制台](http://www.knewron.co.in/saas/1btn/webmain.php)，在那里你可以设置一个账户，配置设备，注册它的 MAC ID，给它分配一个别名，以及[设置它的动作](http://www.1btn.space/systemvariables.php)。1btn 的所有源文件——固件、外壳、原理图、BOM、PCB 布局和示例用例——都发布在他的 [Github 资源库](https://github.com/knewron-technologies/1btn)上。

The [HackadayPrize2016](http://hackaday.io/prize) is Sponsored by: [![Atmel](img/2e52aec37df7a9bb2e83735e78e154fe.png)](http://hackaday.io/atmel)  [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](http://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](http://www.digikey.com/)  [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](http://supplyframe.com/)