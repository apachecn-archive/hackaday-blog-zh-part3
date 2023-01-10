# 为您的 ESP8266 连续交货

> 原文：<https://hackaday.com/2016/06/08/continuous-delivery-for-your-esp8266/>

没什么好羞愧的。这是我们都有的问题。你改变了你的代码很多——你不能帮助它，你只需要调整最后一点点。然后你必须下楼，取出你的 ESP8266 模块，将其插入你的计算机，刷新新的固件，然后跑下来重新安装你的酒窖温度监控器。如果有一种方法可以通过无线方式持续更新您的 ESP8266，从 GitHub 库下载新代码，在其上自动运行您的测试套件，然后将其推送到 ESP，那该多好。

好吧，这是荒谬的矫枉过正，但[squix]把一堆开源持续集成工具串在一起，[让它们与 ESP8266](http://blog.squix.org/2016/06/esp8266-continuous-delivery-pipeline-push-to-production.html) 一起工作。一个简单的 PHP 脚本将 ESP 连接到 web 基础设施的其余部分。

[squix]说“安全”这个词的方式就像杜松子酒爱好者在他们的马提尼酒上低声说“苦艾酒”一样。也就是说，没有。但是对于一个家庭解决方案，或者如果你想玩持续开发，这是一个好的开始。

这是一个很酷的项目，因为它利用了 [ESP8266 OTA](http://esp8266.github.io/Arduino/versions/2.0.0/doc/ota_updates/ota_updates.html#http-server) (空中)编程库来推送代码。我们*确实*讨厌不得不在家里跑来跑去更新固件。

因此，如果您想要将代码推送到您的 ESP8266s，而不需要物理地获取它们，或者如果您想要将您的 web 开发与您的家庭部署集成，请查看它。