# Hackaday 奖参赛作品:CPAP 加湿器监控报警器

> 原文：<https://hackaday.com/2017/08/25/hackaday-prize-entry-cpap-humidifier-monitor-alarm/>

CPAP(持续正压通气)机器可以改变睡眠呼吸暂停患者的生活。[Scott Clandinin]从他的 CPAP 机器中受益，并设计了一种方法来进一步提高他的生活质量，这种方法是一种非破坏性的修改来监控他机器的加湿器。

使用 CPAP 机器，佩戴者呼吸的所有空气都是通过机器的空气。[Scott]的 CPAP 机器有一个小储水器，在空气到达佩戴者之前，它被加热以加湿空气。然而，根据条件的不同，储水器在使用过程中可能会变干，导致使用者醒来时变干并感到不舒服。

为了以一种不需要修改机器本身的非侵入性方式解决这个问题，[Scott]创造了一种由两部分组成的装置。第一部分是 CPAP 机器赖以存在的平台。与 HX711 称重传感器放大器连接的称重传感器允许 Arduino Nano 测量 CPAP 机器和集成水箱的质量。通过定期测量，Arduino 可以检测到蓄水池即将干涸，并发出警报。一个人的睡眠被闹钟打断并不是一种令人愉快的醒来方式，但这比一会儿呼吸热而干燥的空气而变得干燥和不舒服要令人愉快得多。

该装置的第二部分是一个简单的按钮，连接到面罩本身的挂钩上。当屏蔽被挂起时，系统是空闲的。当掩模从挂钩上取下时，系统进行测量并开始工作。这使得激活没有麻烦，更不用说还避免了虚假警报，而用户删除和填充水箱。

对医疗或其他健康相关设备进行非侵入性修改是常见的，非侵入性接口的一个完美例子是赢得 2015 年 Hackaday 奖的[Eyedriveomatic](http://hackaday.com/2015/11/17/the-gaze-controlled-wheelchair-that-won-the-hackaday-prize/)。此外，HX711 称重传感器放大器有一个 Arduino 库，该库曾用于[的浴室秤 refurb 项目](http://hackaday.com/2016/01/16/weighing-scale-gets-a-refurb/)。

The [HackadayPrize2017](https://hackaday.io/prize) is Sponsored by:[![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Texas Instruments](img/3734f1c96ffff85ea2a7eaddc92844ba.png)](https://hackaday.io/ti)