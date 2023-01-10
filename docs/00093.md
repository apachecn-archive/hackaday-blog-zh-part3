# 对过时的安全系统进行逆向工程

> 原文：<https://hackaday.com/2015/09/15/reverse-engineering-an-obsolete-security-system/>

[Veghead]最近去了一个剩余仓库，里面装满了 VHS 剪辑工作室、IBM 键盘、40 年前的电子设备和许多无用的垃圾。他的收获包括一个散发着 20 世纪 80 年代未来主义气息的旧报警系统的木制键盘，他认为将这个连接到 2015 年的报警系统会很酷。他是怎么做到的？[带软件定义无线电](http://fatsquirrel.org/oldfartsalmanac/random/reverse-engineering-a-vintage-wireless-keypad-with-an-rtl-sdr/)。

拉开警报面板后，[Veghead]只发现了一块带有 9V 电池连接器的单面板。警报回路没有螺丝端子，这意味着整个系统是无线的——对于 80 年代中期的硬件来说，这是一个令人印象深刻的成就。快速搜索 FCC 网站显示，这个警报面板注册了两个频段，319MHz 和 340MHz，正好在 RTL-SDR USB 电视调谐器加密狗的范围内。

在捕获一些原始数据并在 Audacity 中回放后，[Veghead]发现了一个简单的 OOK 协议，它为每个密钥发送两个相同的二进制模式。[一个简单的程序](https://github.com/veghead/vintage-wireless-keypad/blob/master/cletus.cpp)获取每次按键的原始位模式，并将它们编码到十二个按钮的映射中。

虽然无线电仍然工作，但[Veghead]发现他的 RTL-SDR 捕获的波形是射频所厌恶的。这个安全系统中的所有组件都已经超过 30 年了，现在肯定有些组件已经不符合规格了。尽管如此，[Veghead]还是能够让这个东西再次工作，这证明了一个 20 美元的 USB 电视调谐器的实用性。

感谢[Jose]发送此邮件