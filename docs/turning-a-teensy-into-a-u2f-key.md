# 将青少年变成 U2F 键

> 原文：<https://hackaday.com/2015/11/09/turning-a-teensy-into-a-u2f-key/>

上个月，GitHub 用户只需花 5 美元就能买到一个特别版的通用第二因子(U2F)安全密钥。[Yohanes]买了两个，但想知道他能否将 U2F 带到其他微控制设备上。他最终用一个小小的 LC 制造了一把 U2F 钥匙，并在这个过程中把 U2F 带给了无知的大众。

通用第二因素正是它在罐头上所说的:它不取代你的密码，但它确实提供了一点额外的验证，以证明登录帐户的人确实是应该登录的人。目前，谷歌(通过 Gmail 和 Google Drive)、Github、Dropbox，甚至 WordPress(通过插件)都支持 U2F 设备，所以能够提供 U2F 的微型 USB key 是一个非常有用的设备。

在深入研究了 U2F 规范之后，Yohanes 发现 Teensy LC 将是一个完美的实验平台。一个 U2F 设备只是一个 USB HID 设备，青少年可以轻松使用。一个方便的库[承担了 AVR 和 ARM 平台的 ECC](https://github.com/kmackay/micro-ecc)和【约哈内斯】[完成的 U2F 实现](https://github.com/yohanes/teensy-u2f)能够把小小的 LC 变成 GitHub 售价 5 美元的东西。

应该注意的是，自己用自己的代码做任何与安全性*相关的事情都是愚蠢的，不应该被认为是安全的。此外，[Yohanes]不想在他的小 LC 上焊接一个按钮，所以他实现了所有的功能，而没有按钮，这也是不安全的。“密钥句柄”只是用固定密钥进行 XOR 加密，也是不安全的。尽管如此，这仍然是一个有趣的项目，我们很高兴[约汉斯]与我们分享它。*