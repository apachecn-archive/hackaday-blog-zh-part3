# 不知何故，建造物联网钻床

> 原文：<https://hackaday.com/2016/12/06/building-an-iot-drill-press-for-reasons-unknown/>

他对原因守口如瓶，但(伊万·米兰达)计划在互联网上安装一台钻床。那会有什么问题呢？

我们会相信[Ivan]的话，他说这种疯狂是有方法的，只是看一看建造本身，希望它能激励一些人把他们卑微的钻床变成有点像 2 轴铣床的东西。[Ivan]广泛使用他的 3D 打印机来制造 X 轴滑块，该滑块用螺栓固定在普通钻床工作台上。在任何人指出显而易见的事实之前，[Ivan]已经承认滑块太脆弱了，经不起太严重的钻孔，特别是考虑到他用来取代动力 Z 轴的套筒柄的齿轮装置的巨大机械优势。电机开关也换成了固态继电器。步进器、继电器和限位开关都被馈入一个与 ESP8266 对话的 Teensy，该 ESP8266 可能会拥有一个网络接口来将这个东西放到网上。

休息后，钻床的相关方面变得更加清晰。

 [https://www.youtube.com/embed/in7QHbu4Z2U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/in7QHbu4Z2U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



原来[Ivan]心中有一种互联网行为艺术作品,其中他网站的访问者将投票决定两部手机中的哪一部将被执行致命的钻压。这个项目失败的方式是多方面的，从网站错误，让第一个访问者在上线八分钟内选择手机，到步进器无法驱动羽毛笔，到廉价手机上令人惊讶的坚固屏幕。哦，好吧，这些失败是对物联网在不久的将来的弊病的一个很好的讽刺。

 [https://www.youtube.com/embed/OF6p4QQ3iG8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/OF6p4QQ3iG8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



也许你会喜欢这些其他的钻床技巧，像[把钻床变成主轴砂光机](http://hackaday.com/2014/04/12/turn-your-drill-press-into-a-bobbinspindle-sander/)，甚至[给台式冲床一个立柱移植](http://hackaday.com/2016/04/16/building-a-taller-drillpress/)以允许更大的工件。

[通过 [r/Arduino](https://www.reddit.com/r/arduino/comments/5dxx5w/i_converted_a_drill_press_to_an_iot/)