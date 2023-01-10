# 彩色编码钥匙打开大门，机会

> 原文：<https://hackaday.com/2018/03/09/color-coded-key-opens-doors-opportunities/>

在所有开锁的方法中，有一些屡试不爽的方法。钥匙、密码、RFIDs、拨片和炸药都有它们的时代和位置，但现在有人想尝试一些新的东西。[Erik]想出了一种锁，当它被展示一种颜色图案时就会打开。

问题中的锁使用一套彩色编码卡作为“钥匙”。当卡插入锁中时，TCS230 颜色传感器解释卡上的图案，并将信息发送到 Arduino Uno。从那里，Arduino 可以命令物理锁打开，如果模式是匹配的，虽然[Erik]仍然在等待锁定机制的到来，同时他继续制作设备的原型。

这是一个相当独特的想法，有很多好处。首先，密码不能像 RFID 卡那样从钱包里被“偷走”。(尽管如果你能拍下卡片的照片，所有的赌注都取消了。)如果您丢失了密钥，您可以简单地打印另一个密钥，该设备能够处理多个不同的密钥，并记录每个密钥的使用情况。此外，与依赖磁条的技术不同，制造卡不需要专门的设备。当然，如果你想用老一套的方法锁上门，总会有这种经典的开门方式。

 [https://www.youtube.com/embed/LEvPNRoVrrA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/LEvPNRoVrrA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

