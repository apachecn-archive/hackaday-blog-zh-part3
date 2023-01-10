# Hackaday 奖品入口:一个移动电动门

> 原文：<https://hackaday.com/2017/06/16/hackaday-prize-entry-a-mobile-electric-gate/>

电动门可以是一个很好的省力装置，当门通过远程激活打开和关闭时，人们可以留在车内。然而，在各种所需的遥控器和遥控器之间周旋可能会变得有些麻烦，因此[bredman]设计了一个替代解决方案—[通过移动网络控制电动门。](https://hackaday.io/project/25294-gsm-connected-remote-electric-gate)

20 年前，这可能是通过将一系列继电器连接到车载电话的振铃器来实现的。如今，它变得更加复杂——GSM/GPRS 模块连接到 Arduino Nano。当检测到来电时，门就会打开。等待 3 分钟后，闸门再次关闭。

[bredman]在项目过程中遇到了一些挫折，原因是在 Arduino Nano 上使用串行和在 A6 GSM 模块上使用复位线时出现了一些意外。然而，总的来说，闸门是一个简单的接口设备，就像许多这样的设备一样，它有很好的标记和记录的引脚，用于发送闸门打开和关闭信号。

[bredman]精心设计系统以避免不必要的操作。系统被设计为总是自动关闭闸门，因此无论控制器被调用多少次，闸门将总是以关闭状态结束。还特别注意确保控制器能够优雅地处理与移动网络的连接丢失。像这样的选择可以让一个项目使用起来更令人满意——一个不断需要关注和重启的 gate 系统可能不会持续很长时间。

总的来说，这是一个伟大的项目，表明了此类项目是多么容易实现——通过一些精心选择的模块和对串行通信的掌握，将一个项目连接到互联网或移动网络几乎是轻而易举的事情。换个角度，看看这个记录到 Google Drive 的[车库门开启器。](https://hackaday.com/2017/01/15/garage-door-opener-logs-to-google-drive/)

The [HackadayPrize2017](https://hackaday.io/prize) is Sponsored by:[![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Texas Instruments](img/3734f1c96ffff85ea2a7eaddc92844ba.png)](https://hackaday.io/ti)