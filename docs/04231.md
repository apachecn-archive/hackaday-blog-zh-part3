# “Alexa，让我的 ESP8266 做点什么”

> 原文：<https://hackaday.com/2016/11/23/alexa-make-my-esp8266-do-something/>

亚马逊 Echo 及其小巧的 Dot 表兄弟具有能够控制一些家庭自动化设备的便利功能。如果你拥有正确的制造商的硬件，你可以单独使用你的声音的力量来弯曲你的家。

问题是，如果你的硬件不在受支持的设备列表上，或者你是自己做的，那你就不走运了。

[Xose Pérez]通过使用运行一组模拟 Belkin WeMo 设备的脚本的服务器来回避这个问题，Echo 支持该设备。服务器可以向他的微控制器发出命令，但他想要更多。为什么不去掉中间环节，将 WeMo 仿真直接集成到完成这项工作的 ESP8266 上呢？

他采用了他一直使用的 Fauxmo Python WeMo 模拟器，并将其移植到一个 ESP8266 库中，该库可以合并到现有代码中，使其作为 WeMo 设备出现在世人面前。他在代码页和上面链接的页面上提供了完整的指令[。](https://bitbucket.org/xoseperez/fauxmoesp)

他承认他不是第一个实现这个目标的人，并提到了这个更早的项目。然而，他要求将一个库合并到另一个软件中，但这并没有满足他的要求，因此他的工作。

我们喜欢这个项目，但可能值得提醒读者的是，Alexa 确实有一个以 [Alexa 技能工具包](http://hackaday.com/2015/12/26/let-alexa-control-your-life-guide-to-voice-enable-everything/)形式存在的 SDK。你可以用它来做各种聪明的事情，用你的回声或圆点…或者你可以[让它成为大嘴比利巴斯新奇装饰品](http://hackaday.com/2016/11/08/alexa-brings-back-singing-fish-this-time-its-a-good-thing/)的大脑。