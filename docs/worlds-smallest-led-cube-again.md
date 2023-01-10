# 世界上最小的 LED 立方体——再次出现

> 原文：<https://hackaday.com/2017/01/30/worlds-smallest-led-cube-again/>

“[世界上最小的 4x4x4 RGB LED 立方体](http://www.instructables.com/id/LED-Cube-Pendant/)”的头衔有了新的挑战者。[nqtronix]的 13x13x36 毫米的立方体吊坠比[[Hari fun 的](http://hackaday.com/2016/02/05/building-the-worlds-smallest-rgb-led-cube/)版本小得多，加上外部电子设备，立方体的尺寸约为 17x17x17 毫米。[nqtronix]花了大约一年时间才获得这个位置，从评论部分来看，[HariFun]似乎没有抱怨。这个立方体吊坠足够小，可以用作钥匙链，而且[nqtronix]已经设法在里面塞进了很多电子设备。

使用的 LED 是 1.6 平方毫米的 0606 RGB，尽管他在放弃这个想法之前确实考虑过使用 0404。有许多方法可以驱动 192 个 IO，但在这种情况下， [Charlieplexing](https://aglick.com/charliecube.html) 似乎是最好的解决方案，需要 16 个 IO。与[HariFun]的构建不同，这款是完全集成的，微控制器、电池和其他所有东西都包装在一个完全由 PCB 制成的外壳中——灵感来自[Voja Antonic]的[FR4 外壳技术](http://hackaday.com/2015/06/03/how-to-build-beautiful-enclosures-from-fr4-aka-pcbs/)，LED 阵列嵌入在透明树脂中。

一路走来，他不得不求助于几个黑客来实现它。首先，他使用了 [ATmega328BP](http://www.atmel.cimg/Atmel-42559-Differences-between-ATmega328P-and-ATmega328PB_ApplicationNote_AT15007.pdf) [pdf]，而不是更常见的 ATmega328P，这给他额外的 IO 来玩。由于 Charlieplexing 在更高的电压下工作得更好，他使用升压转换器来提供+5.5V 的最大电压。ATmega 的限制—驱动立方体。LiPo 充电器有一个稍微不同寻常的 P-MOSFET 开关部分，可以在 USB 输入和 LiPo 之间切换，而不会导致太多的压降。有几个部分有助于检测低电压，但他的代码还没有使用这个功能。他还在混合中加入了一个加速度计，以响应点击、双击和摇动，但这也尚未在代码中实现。因为他耗尽了电路板空间，EEPROM 是死虫焊接。这个按钮是从一个普通的按钮上拆下来，利用它的内部构造而成的。他在 Instructable 上发布了 DIPtrace 板的设计文件和代码，以防有人想尝试复制这个立方体。虽然我们必须说，除了是一个焊接忍者，你还需要相当好的机械印章来建立这个小立方体。