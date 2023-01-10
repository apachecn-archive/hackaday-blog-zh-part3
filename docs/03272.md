# Hackaday 奖品入口:投票站投票

> 原文：<https://hackaday.com/2016/08/15/hackaday-prize-entry-polling-the-polling-places/>

15 年前，一名开发人员作证说，他受雇编写代码，利用电子投票机操纵选举。在今年的总统初选中，出口民调明显不同于官方结果，但只是在使用无法验证的电子投票机的选区。民主只有在投票过程的完整性能够得到保证的情况下才能存在，而且没有一个国际选举监督委员会来核实美国每个选区的选举。

您的投票可能不算数，但这并不意味着您应该等待几个小时来投票。这个 Hackaday 奖旨在通过给选民一个方便的应用程序来检查他们即将面临的等待时间，从而结束投票站的过长等待时间。

Qubie 是一种简单记录选民在投票站排队等候时间的设备。这背后的技术非常简单——只需要一个树莓皮、WiFi 适配器和一块电池。该设备通过查看智能手机提供的 WiFi 来跟踪选民排队等候的时间。这些数据，其中有一个 MAC 地址，是伪随机的，大约每分钟检查一次，以便很好地了解特定智能手机在 Pi 范围内有多长时间。这些数据然后被广播到服务器，服务器计算出在特定的投票点需要等待多长时间。

在最近的加州初选中，沙斯塔县的十个投票点使用了 Qubie。他们记录了总共超过 3 万次的 WiFi 联系，在粗略检查数据后，看到了你会预料到的现象:午餐时间和一天结束时活动激增。这是一个伟大的项目，收集应该自动化和公开的数据，也是 Hackaday 奖的一个伟大的参赛作品。

The [HackadayPrize2016](https://hackaday.io/prize) is Sponsored by:[![Atmel](img/2e52aec37df7a9bb2e83735e78e154fe.png)](https://hackaday.io/atmel) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://www.digikey.com/) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/)