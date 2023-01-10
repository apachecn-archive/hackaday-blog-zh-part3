# USB Arduino 到 AVR TPI 编程器

> 原文：<https://hackaday.com/2017/01/06/usb-arduino-into-avr-tpi-programmer/>

将几乎任何种类的 Arduino 变成简单的 AVR 6 针 ISP 程序员都是老一套了。但是当 Atmel 推出一系列非常小的 AVR 芯片时，ATtiny10 和 friends 总共只有 6 个引脚，他们需要一个新的编程标准。进入 TPI(微型编程接口)，退出所有你以前有用的 DIY AVR 程序员。

[Kimio Kosaka]为 ATmegaxxUn 芯片编写了一个[两用 TPI 和 ISP 固件](http://make.kosakalab.com/make/electronic-work/avrisp-mk2/uno-r3_avrisp-mk2_en/)，该芯片在 Unos 上用作 USB 串行桥，并构成了 [Leonardo 或 Micro](http://make.kosakalab.com/make/electronic-work/avrisp-mk2/leo-r3_avrisp-mk2_en/) 上唯一的芯片。有什么问题吗？你需要做一点细微的焊接。具体来说，[小坂先生]希望你通过钻一个通道来获得一个原本模糊的信号。我们会为此而努力。

剩下的程序是将一个 DFU USB 引导加载程序刷新到 Arduino 中，然后加载 flash 编程器代码。你以前的 Arduino 现在可以闪存老式 ISP AVR 芯片，以及需要 TPI 的小芯片。

如果你有似曾相识的感觉，是的，我们之前介绍过一个 [DIY TPI 程序员](http://hackaday.com/2012/08/23/programming-the-attiny10-with-an-arduino/)，但是它需要在你的主机上安装一个定制的上传软件。[Kosaka]的版本作为 Atmel 程序员出现在主机上，您可以使用任何标准工具。你可以尝试一些有趣的精细焊接工作。这是双赢！