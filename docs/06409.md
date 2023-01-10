# 监测你所在城市的空气质量

> 原文：<https://hackaday.com/2017/07/16/monitor-your-citys-air-quality/>

[Radu Motisan]在 2017 年 Hackaday 奖中的参赛作品是一系列物联网空气质量监测器，即[城市空气质量](https://hackaday.io/project/8334-city-air-quality)项目。根据 Radu 的说法，空气污染是欧洲城市过早死亡的最大环境原因，而交通是主要来源。[Radu]创造了一种可以在整个城市部署的装置，它上面有传感器来报告空气质量。

硬件有一个用于颗粒物质的激光散射传感器和 4 个用于一氧化碳、二氧化氮、二氧化硫和臭氧的机电传感器(这些传感器检测多个国家公认对健康有重大影响的六个参数。)这些传感器有两年的寿命，所以它们被安装在插座上以便于更换，如果需要，你可以换成不同的传感器来检测不同的东西。用于硬件的 PCB 分为 WiFi 版本和 LoRaWAN 版本，软件在 ATMega328 上运行 PCB 具有用于编程的标准六引脚 ISP 连接。

收集的数据被发送到服务器，在服务器上根据设备的校准参数进行调整，并存储在每个传感器的数据库中。这使得在传感器寿命结束时对其进行维修变得更加容易，因为所需要的只是更换单元中的传感器和改变为该单元存储的校准参数，而这需要改变软件。服务器通过 RESTful API 提供数据，因此用统计数据和图表构建仪表板变得很容易。

[Radu]使用现成的模块作为第一个原型，并将其连接到汽车上，同时四处行驶。他用这个来测试计划并在服务器上工作。然后，他开始为最终单元设计 PCB 硬件和外壳。这项工作是[Radu]之前工作的延伸，在 2015 年 Hackaday 奖中突出了这里的，但也检查了这个将[空气质量传感器放在教室的项目](https://hackaday.com/2016/06/18/air-quality-sensors-in-every-classroom/)。

 [https://www.youtube.com/embed/REUyFWeUg5k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/REUyFWeUg5k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2017](https://hackaday.io/prize) is Sponsored by:[![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Texas Instruments](img/3734f1c96ffff85ea2a7eaddc92844ba.png)](https://hackaday.io/ti)