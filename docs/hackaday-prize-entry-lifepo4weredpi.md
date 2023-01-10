# Hackaday 奖参赛作品:LiFePO4wered/Pi+

> 原文：<https://hackaday.com/2017/05/26/hackaday-prize-entry-lifepo4weredpi/>

对于你们中的一些人来说，这个标题可能看起来很熟悉，因为[Patrick Van Oosterwijck]life po 4 wered/Pi 项目是一个非常成功的 Hackaday.io 项目。现在，他正在从头开始设计*加*版本，以填补一些空白，解决一些影响最初项目的挑战。那么[life po 4 wered/Pi+](https://hackaday.io/project/20909-lifepo4weredpi)到底是什么，能做什么？

简而言之，这是一个智能 UPS 的树莓派。标准版本允许 A+和 Pi Zero 使用电池运行超过 2 小时，B+、B2 和 B3 运行至少 1 小时(当然，可能会更短，取决于系统负载)。它通过 I2C 总线实现了电源系统和 Raspberry Pi(运行开源守护程序)之间的双向通信。这允许连续测量电池电压和负载电压，用户可编程阈值用于启动、干净关断和硬关断。有一个触摸板，即使在无头设置中也能提供干净的启动/关闭功能，有一个唤醒定时器，允许 Raspberry Pi 在低占空比应用程序中关闭，还有一个自动启动功能，通过在电池电量充足时让 Raspberry Pi 运行来最大限度地延长正常运行时间。

那是标准版本，我们去年报道过的……还有什么是*加*的版本？

嗯，首先，它带来了更多的电流运行完整的系统与液晶显示屏和硬盘驱动器，以前的版本是有限的，当它来到当前。它将为更广泛的输入电源提供选择，如太阳能电池板，这很好。开/关按钮和电源 led 将不再焊接在主板上，因此它们可以“重新定位”到其他地方，例如在制作定制外壳时。将增加检测输入电源以触发自动启动和关闭，最后，但并非最不重要的是，一个具有绝对时间唤醒的实时时钟。

这就是新的 LiFePO4wered/Pi+版本，为树莓 Pi 爱好者提供了所有的功能。

The [HackadayPrize2017](https://hackaday.io/prize) is Sponsored by:[![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Texas Instruments](img/3734f1c96ffff85ea2a7eaddc92844ba.png)](https://hackaday.io/ti)