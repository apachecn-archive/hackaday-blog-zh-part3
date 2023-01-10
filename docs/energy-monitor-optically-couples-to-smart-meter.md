# 电能监控器光学耦合至智能电表

> 原文：<https://hackaday.com/2016/04/24/energy-monitor-optically-couples-to-smart-meter/>

黑客喜欢监控事物。无论是外部温度还是洗澡所用的能源，建立一个传感器并显示数据的实时图表是黑客的天堂。但是，最有趣的图表来自于对整体用电量的监控，这就是这款光耦合智能电表监控器的用武之地。

[Michel]的抄表器非常简单。他的智能瓦特计配备了一个红外 LED，可以显示消耗的每瓦特小时，因此光学耦合是一种自然的方法。脉冲本身只有 10 毫秒宽，所以他建立了一个脉冲展宽器来调节 PIC 微控制器的脉冲。PIC 还通过 DS18B20 读取外部温度，并将所有信息反馈给中央电源监控器，通过 LCD 显示屏和经典的 Simpson 电表显示当前的用电量。中央监控器向 Thingspeak 发送电力和温度数据，以及来自[Michel]的[柴炉监控器](http://hackaday.com/2016/02/08/a-wireless-wood-stove-monitor/)和一个尚未实现的热水器监控器的数据。

[Michel]正在为他在魁北克的运营基地建造一套令人印象深刻的能源和环境监控器。我们期待看到他是如何监控热水器的，也期待看到他想出的其他主意。

 [https://www.youtube.com/embed/CMCYLAV8Ct0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/CMCYLAV8Ct0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

