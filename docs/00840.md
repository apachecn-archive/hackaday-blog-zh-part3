# 无线水表监控器手表浪费

> 原文：<https://hackaday.com/2015/12/06/wireless-water-meter-monitor-watches-waste/>

黑客喜欢衡量事物，这不是什么秘密。好的数字会带来好的决定，比如什么时候把你的浪费少年踢出奢华冗长的淋浴。因此，这款基于 Arduino 的无线水表接口应运而生。

我们会说“无线”有点夸张。创造者[大卫·施奈德]选择将系统分为两部分——一个磁力计和一个 Arduino 来感应自来水公司电表的脉冲，一个 Raspberry Pi 来服务网络界面。水表在街上，而不是在他的房子里，所以传感器通过电话线连接到 Pi。但是从那里系统是无线的。

[David]详细介绍了他所面临的传感问题，该问题依赖于检测流量计内部旋转位产生的变化磁场，并使用 Arduino 清理信号；他还解决了当流速接近磁力计采样速率时出现的混叠误差。

我们喜欢这样一个事实，即利用这种技术来监控旋转磁场的其他过程有很大的潜力。就像[这种光学耦合的燃气表监控器](https://hackaday.com/2015/06/30/disassembled-mouse-keeps-track-of-gas-meter/)一样，它也不会侵入电力公司的设备，这是一个优点。

[via [reddit](https://www.reddit.com/r/arduino/comments/3v07y7/a_wireless_arduino_powered_water_meter/)