# Hackaday 奖参赛作品:MyComm 手持卫星信使

> 原文：<https://hackaday.com/2016/06/27/hackaday-prize-entry-mycomm-handheld-satellite-messenger/>

我们生活在一个互联的世界，但这个世界的尽头就在最外面的手机信号塔不远处。[约翰·格兰特]希望在任何地方都能联网，甚至是在没有移动网络的地区，所以他正在建造一个[太阳能手持卫星信使:my comm](https://hackaday.io/project/11802-mycomm)——他的黑客日奖参赛作品。

MyComm 是一种手持式触摸屏设备，很像智能手机，它连接到铱星卫星网络来发送和接收文本消息。在他建造的核心，[约翰]使用 RockBLOCK Mk2 铱星卫星通信模块连接到一个 Teensy 3.1。固件基于 [FreeRTOS 端口](https://forum.pjrc.com/threads/26411-FreeRTOS-8-0-1-for-Teensy-3-x-Due-and-AVR-boards)构建，用于适当的任务管理。项目贡献者[Jack]精心制作了一个直观的 GUI，包括一个屏幕键盘来编写、发送和接收消息。微型 SD 卡存储所有信息和联系人列表条目。最终，该系统将配备太阳能电池、充电调节器和 LiPo 电池，用于全球无条件连接。

对于铱星网络来说，2016 年将是有趣的一年，因为改进的(向后兼容的)“铱星 NEXT”网络的第一批卫星预计将很快发射。由于可靠性和安全性的不足，目前覆盖全球的 66 颗铱星卫星有时被认为是价值 50 亿美元的太空垃圾。然而，它仍然存在，制造商友好的调制解调器售价为 250 美元，按使用付费的费率约为 7ct/kB(SDR 黑客免费下载)。欣赏[Jack]解释 MyComm 用户界面的视频:

 [https://www.youtube.com/embed/ZtoFjqGbMIs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ZtoFjqGbMIs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2016](http://hackaday.io/prize) is Sponsored by: [![Atmel](img/2e52aec37df7a9bb2e83735e78e154fe.png)](http://hackaday.io/atmel)  [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](http://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](http://www.digikey.com/)  [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](http://supplyframe.com/)