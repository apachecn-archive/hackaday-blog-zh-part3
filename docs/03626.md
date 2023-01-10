# 黑客日奖参赛作品:忒伊亚物联网电灯开关

> 原文：<https://hackaday.com/2016/09/24/hackaday-prize-entry-theia-iot-light-switch/>

在英国电灯开关的标准外形中，似乎没有无线启用的电灯开关。至少，那是[loldavid6]的经历，当时他决定需要一个。此外，他能找到的开关都不是开源的，也不容易集成。所以他开始设计自己的产品，忒伊亚物联网灯开关就是这个成果。

在采用标准的电灯开关时，他担心他的装置不会依赖于开关的位置来操作。因此，他必须确保开关仅仅是他设计的电路板的输入，而不是控制电源。他选定 ESP8266 无线微控制器作为该装置的大脑，继电器负责电源开关。他首先考虑使用一个 [LNK304](https://ac-dc.power.com/products/linkswitch-family/linkswitch-tn/) 离线开关 PSU 芯片来获得他的低电压，但后来转向了现成的开关模式板。

到目前为止，已经完成了两个原型设计，每个电源选项一个。已经订购了电路板，他现在正处于国际邮资的漫长等待期。所有的 KiCad 和其他文件都可以从项目的 hackaday.io 页面下载，所以如果你愿意的话，你可以自己看看。

你可能会问为什么可能需要另一个物联网灯开关。但是，即使它们现在已经可用并且便宜，仍然存在一个开放的板的差距，更重要的是不依赖于其他人的云后端。另外，当然，这块板不仅仅可以用来照明。

灯泡图片:осадчаяекатерина(自己的作品)[CC BY-SA 4.0]，via [维基共享资源](https://commons.wikimedia.org/wiki/File:An_indispensable_source_of_light_your_time.jpg?uselang=en-gb)。

The [HackadayPrize2016](https://hackaday.io/prize) is Sponsored by:[![Atmel](img/2e52aec37df7a9bb2e83735e78e154fe.png)](https://hackaday.io/atmel) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://www.digikey.com/) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/)