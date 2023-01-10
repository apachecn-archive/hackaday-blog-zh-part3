# 研究人员破解蓝牙枪支保险箱

> 原文：<https://hackaday.com/2017/12/13/bluetooth-gun-safe-cracked-by-researchers/>

信不信由你，有相当多的人购买了可以通过蓝牙远程解锁的枪支保险箱。现在我们可以理解*为什么*有人可能认为这是一个好主意:能够在最激烈的时刻按下手机上的按钮并准备好武器的便利性可以说是购买这种东西用于家庭防御的人的一大卖点。但那些更有技术头脑的人可能会想，让你的枪支(或其他贵重物品)受到协议保护的内在风险，是否比不需要在键盘上输入密码的便利更重要。协议通常依赖于模糊的安全性。

嗯，你不会再感到惊讶了，因为【两个六个实验室】的研究人员最近发表了一份详细的文件，介绍他们如何设法远程解锁 vault AK VT20i，而没有比 [Ubertooth](https://hackaday.com/2011/02/09/ossmann-talks-about-ubertooth-at-schmoocon/) 更奇特的东西。最后，甚至 Ubertooth 实际上并不需要，因为这种特殊的设备被证明充满了安全问题。

[Two Six Labs]没有公开发布他们在 YouTube 视频中演示的软件的完整源代码，原因很明显，但他们网站上的页面确实非常详细地介绍了他们如何发现允许他们编写该软件的多个漏洞。即使你不是那种需要枪支保险箱的人，他们的文档中包含的关于分析蓝牙通信的信息也是非常有趣的。

人们发现，保险箱的 PIN 码实际上是由附带的智能手机应用程序以纯文本形式传输的，这在正常情况下已经足够糟糕了。但是经过进一步的分析，很明显这个保险箱根本就没有检查密码。

[![](img/19661b256d7b2a47a49adaca1ec9866c.png)](https://hackaday.com/wp-content/uploads/2017/12/bluesafe_detail.png)

Scripting app interactions with ADB and Python

对于额外的风格点，[Two Six Labs]还展示了一种使用 Vaultek Android 应用程序暴力破解 PIN 的方法，方法是编写一个 Python 脚本，按顺序输入代码，直到找到正确的代码；开发者甚至懒得对失败的尝试进行限制。

对于一个表面上被设计为包含致命武器的设备来说，[两个六个实验室]的团队发现的安全缺陷是绝对不可原谅的。但是有一个积极的结果，因为制造商发誓要更新易受攻击的保险箱，并在未来做出更大的努力，更严格地设计和测试他们的蓝牙实现。这是负责任的披露的目标，我们很高兴看到制造商做正确的事情

[蓝牙控制锁的安全问题是众所周知的](https://hackaday.com/2016/12/28/33c3-breaking-iot-locks/)，所以像这样的设备仍然被遗漏，这有点令人失望。[我们建议你对任何利用蓝牙](https://hackaday.com/2016/08/08/the-terrible-security-of-bluetooth-locks/)的安全设备保持怀疑，直到行业开始更认真地对待事情。

 [https://www.youtube.com/embed/1xrdwhisW-M?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/1xrdwhisW-M?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

