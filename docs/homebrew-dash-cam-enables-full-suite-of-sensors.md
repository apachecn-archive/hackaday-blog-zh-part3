# 家酿仪表板摄像头支持全套传感器

> 原文：<https://hackaday.com/2016/12/06/homebrew-dash-cam-enables-full-suite-of-sensors/>

你首先听到的是:仪表盘摄像头将成为你日常驾驶的下一个必备物品。在世界一些地区已经达到市场饱和，但在北美仍然相当少见，我们预测汽车制造商将很快抓住这一趋势，开始为汽车配备仪表板摄像头作为标准设备。你可以打赌，无论他们推出什么淡化的、定价过高的功能集，都肯定会令人失望，所以你可能想考虑用加速度计和大量 LEDS 构建自己的树莓 Pi dash cam。

[CFLanger]的项目仍处于原型阶段，其核心是一个 dash cam，但看起来他想做的远不止这些。Raspivid 和 PI NoIR 摄像头负责视频流，但 Pi SenseHAT 的加入为[CFLanger]提供了一系列感知和记录汽车环境的选项。他不满足于 SenseHAT 的板载加速度计，还在传感器套件中增加了 ADXL345。64 像素的 LED 显示屏只是为了好玩——它可以显示平台的俯仰和滚动——而一个尚未实现的条形图显示屏将显示 X 轴上的加速度。他认为对于几天的视频来说，整个事情是好的，但我们希望他增加音频捕捉，也许还有来自 OBDII 蓝牙适配器的 ECU 数据。

至少到目前为止，我们在 Hackaday 上很少看到 DIY dash 摄像头。已经有[一个仪表板摄像头拆卸和重新分配](http://hackaday.com/2015/02/01/transcend-drivepro-200-hack-to-stream-and-script-begs-for-more/)，还有大量的[仪表板电脑](http://hackaday.com/2015/02/18/custom-double-din-mount-for-nexus-7-carputer/)构建。似乎大多数黑客首先想要那辆 [DIY 自动驾驶汽车](http://hackaday.com/2015/12/17/self-driving-acura-built-in-a-garage/)。

 [https://www.youtube.com/embed/f9TNMCFE1a8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/f9TNMCFE1a8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

