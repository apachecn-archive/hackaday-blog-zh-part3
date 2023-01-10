# 吠叫物联网宠物监控器

> 原文：<https://hackaday.com/2018/01/05/bark-back-iot-pet-monitor/>

当你不在家的时候，你的宠物会难过吗？或者，当你不在的时候，他们的良好行为可能会有所松懈，从而引起邻居的骚动。嗯，[jenfoxbot]就有这样一只狗，所以她建造了一个[‘吠叫’物联网宠物监视器](http://foxbotindustries.com/bark-back-monitor-interact-pets/)来在她外出时照看它。

宠物显示器的大脑和骨干是一直受欢迎的树莓 Pi 3。Sparkfun MEMS 麦克风分线板监听任何不守规矩的行为，MCP3002 模数转换器芯片读取麦克风输入。一些试错编码允许她设置一个噪音阈值，一旦超过，就会触发一个音频文件，让她的狗安静下来。它还记录事件并将任何状态更新上传到 CloudMQTT 服务器，以便在离开家时进行监控。她的 Imgur build 专辑可以在[这里](https://imgur.com/a/b64PP)找到，GitHub 项目页面是[这里](https://github.com/jenfoxbot/BarkBack)如果你想建立自己的！

休息后看看演示视频，这可能会让她的好狗狗 Marley 感到困惑。

 [https://www.youtube.com/embed/JbwuoS_6yl8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/JbwuoS_6yl8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



我们之前展示了一款[联网的零食分配器](https://hackaday.com/2013/02/05/web-connected-treat-dispenser-appeases-the-pets/)，但是你会给一只[机器宠物](https://hackaday.com/2016/03/11/robotic-pets-test-an-automatic-pet-door/)什么样的零食呢？

[通过 [/r/DIY](https://www.reddit.com/r/DIY/comments/7mo1aw/i_made_an_iot_pet_monitor_to_talk_back_to_my_dog/)