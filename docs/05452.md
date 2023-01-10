# 黑掉你的车钥匙可以节省很多钱

> 原文：<https://hackaday.com/2017/03/29/save-big-by-hacking-your-car-keys/>

一把新车钥匙三百块？胡说八道！当你丢失了你的钥匙或者想为那个新的青少年司机做一个额外的，不要让小偷减轻你的钱包。只需[拉动 ECU 并破解一些 hex 来添加新的密钥](https://www.instructables.com/id/DIY-Immobilizer-Hacking-for-Lost-Keys-or-Swapped-E)。

下面的视频是[speedkar9]用来重新编程丰田 ECU 的过程的旋风之旅，以允许新的钥匙通过你的新(er)车的安全测试。自 21 世纪初左右，大多数制造商已经将 RFID 芯片包含在他们的钥匙中，这样只有已知的钥匙才能启动汽车。在丰田汽车中，这是由转向柱中的 RFID 阅读器完成的，它将插入的钥匙代码传递给发动机控制单元。如果 8 字节的密钥代码与存储在 ECU 中的三个值之一匹配，汽车将启动。清除 ECU 中的 EEPROM 是[speedkar9]程序的重点，它连接到 EEPROM 并读取内容。他的装备包括一个 RS-232 串行连接，所以这次黑客攻击最困难的部分可能是用 DB-9 插孔围捕一台 PC，但一旦你完成了这一点，就有点抨击 ECU“处女化”以准备重新编程。

当然，程序的细节会因制造商而异，而且更近年份的汽车可能会有更多的安全问题要担心。你甚至会像黑掉一辆拖拉机一样与 DRM 发生冲突吗？或许吧。但是 300 美元就是 300 美元。

 [https://www.youtube.com/embed/qRz2b1S2PGk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/qRz2b1S2PGk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[darks prte]的提醒。