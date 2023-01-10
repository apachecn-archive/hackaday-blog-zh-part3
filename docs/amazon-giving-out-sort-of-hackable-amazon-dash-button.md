# 亚马逊发布了(某种)可破解的亚马逊破折号按钮

> 原文：<https://hackaday.com/2015/10/11/amazon-giving-out-sort-of-hackable-amazon-dash-button/>

我们已经看到了一些有趣的亚马逊 Dash buttons，一个简洁的设备，你按下一个按钮，它就会为你从亚马逊订购一个产品。现在，[亚马逊]自己正通过 [AWS 物联网按钮](http://aws.amazon.com/iot/button/)享受黑客乐趣。这是一个仪表板按钮，亚马逊在活动中分发，以推广他们的新[亚马逊网络服务(AWS)物联网(IoT)服务](http://aws.amazon.com/)。

作为他们接管世界努力的一部分，AWS 物联网服务允许你创建基于按钮的服务，如订购披萨或启动网飞，但不需要运行自己的服务器。相反，亚马逊在其 Lambda 引擎上处理所有幕后的硬东西，该引擎接收按钮发送的一小部分 JSON，并运行 Lambda 函数，该函数订购披萨，启动网飞，然后引发第三次世界大战。亚马逊提供了一些示例动作，比如~~发射导弹~~ [通过 Twilio](https://www.twilio.com/) 发送文本信息[向数据库写入数据](https://gist.github.com/jinman/2ac9e23ea748b2163cf7)。亚马逊没有出售这些按钮:它们似乎只是在活动中作为赠品出售。在评论区制造足够大的噪音，也许他们会给 Hackaday 社区分配一些。

亚马逊仍然保持硬件的严格封闭，只设计使用他们自己的 Lambda 云服务。这与仪表盘按钮没有什么不同，但你会记得当按钮加入网络时，它们被检测到[而遭到黑客攻击。这已经足够好了，可以做一些事情，比如监控](http://hackaday.com/2015/08/10/hacking-the-amazon-dash-button-to-record-whatever-you-want/)[婴儿的肠道运动](https://medium.com/@edwardbenson/how-i-hacked-amazon-s-5-wifi-button-to-track-baby-data-794214b0bdd8)。

感谢[哈利·埃金斯]的提示！