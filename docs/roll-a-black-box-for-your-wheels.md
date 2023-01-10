# 为你的轮子滚动一个黑盒子

> 原文：<https://hackaday.com/2018/06/06/roll-a-black-box-for-your-wheels/>

25 年前，随着安吉星(OnStar)的首次亮相，车载遥测设备，也就是众所周知的黑匣子，打开了消费市场。现在，如果你想在安全驾驶游戏的折扣中碰碰运气，你可以从你的保险公司免费得到一个。但是如果你想要一个不与世界共享你的驾驶数据的黑匣子呢？[就做一个](http://www.instructables.com/id/DIY-Telematics-Box/)。

[TheForeignMan]的 DIY 远程信息盒旨在通过 ODBII 端口获取汽车的转速、速度和油门踩下角度的报告。ODBII-to-Bluetooth 模块将数据发送到 Arduino Mega，并将其与来自 NEO-6M GPS 模块的纬度和经度一起记录在 SD 卡上。一切都由汽车电池通过点烟器-USB 适配器供电。

他把所有东西都紧紧地包在一个 3D 打印的盒子里，这使得找回 SD 卡非常困难。在未来，他想把数据发送到服务器上，以避免跳线意外脱落。

如果这还不足以让你模仿，那么[开始构建你自己的 CAN 总线阅读器](https://hackaday.com/2012/04/17/tinkering-with-odb-ii-and-the-can-bus/)。