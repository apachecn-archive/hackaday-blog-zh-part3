# Hackaday 奖参赛作品:平装桌面 EPaper 显示器

> 原文：<https://hackaday.com/2017/10/11/hackaday-prize-entry-paperback-desktop-epaper-monitor/>

当我们宣布 Hackaday 奖及其最佳产品类别时，[PK]询问了他的妻子和同事关于使用 6 英寸 800×600 ePaper 制作桌面显示器的想法，他已经制作了这款显示器，并将其称为平装版。对显示器的一个这样的要求是能够使用通常的桌面方法之一连接到它:VGA、DVI 或 HDMI。鉴于他之前为 2015 年的奖项制作自己的 VGA 卡的经历[，他选择了那个。HDMI 正在研发中。](https://hackaday.io/project/6309-vga-graphics-over-spi-and-serial-vgatonic)

但它最终不仅仅是一个桌面显示器。他首先制作了一个电源和分线板，VGA 输入板最终会连接到这个分线板。为了测试它，他包括了一个用于插入 ESP32 的插座。他只有一个胸围，在电子纸上展示了 Hackaday 的标志。他现在还可以选择将它用作无线互联网连接显示器。

转到 VGA 支持，[PK]使用 MST9883 芯片制作了一个 VGA 输入板，它可以对 VGA RGB 图形信号进行模数转换，还可以从 HSYNC 恢复像素采样时钟。他的新 VGA ePaper 显示器必须向 VGA 源标识自己，告诉它尺寸、分辨率等等。这被称为 [EDID](https://en.wikipedia.org/wiki/Extended_Display_Identification_Data) ，通过在电路板上增加一个 Atmel ATmega328 来处理。最后，LCMXO1200C FPGA 在 4 MBit SRAM 帧缓冲器的帮助下完成高速转换。

他的第一个测试只是使用 ESP32 显示 Hackaday 徽标，但现在使用 VGA 输入板，他可以显示 Doom。由于它使用 ePaper，它只有 1 秒的刷新率，但很难想出一个更好的方法来证明它的工作。他也可以随时拔掉，原封不动地拿着最新的截图走人。下面的视频自己看吧。

 [https://www.youtube.com/embed/Fd8cFR_uTQM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Fd8cFR_uTQM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



如果你想制作自己的平装本，【PK】已经[把它彻底](https://hackaday.io/project/21607-paperback-desktop-epaper-monitor)文档化了，包括[GitHub](https://github.com/dqydj/PaperBack_EPaper_Display/)上的所有代码和原理图。

破解这些 ePaper 显示器非常有趣，我们已经在 Hackaday 上看过几次了。一个非常酷的例子是名片上的电子名片。在明亮的阳光下阅读是最棒的，这就是为什么[迈克·霍尔登]为[改装了一台电子阅读器，用来显示他在帆船](https://hackaday.com/2012/09/07/adding-epaper-navigation-data-to-a-sailboat/)上的天气。

The [HackadayPrize2017](https://hackaday.io/prize) is Sponsored by:[![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Texas Instruments](img/3734f1c96ffff85ea2a7eaddc92844ba.png)](https://hackaday.io/ti)