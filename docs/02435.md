# 最酷但最不安全的安全设备

> 原文：<https://hackaday.com/2016/05/28/coolest-but-least-secure-security-device/>

[Matikas]当他起床去买咖啡时，显然忘记了锁定他的电脑屏幕。他显然和一群鲨鱼一起工作:“如果你不(锁定它)，你的一个同事会给整个公司发电子邮件，说你邀请他们去喝啤酒(当然是在你的账单上)。”提醒你一下，不是说我们没有做过类似的事情。无论如何，在办公环境中忘记锁屏是一件严肃的事情。

所以[Matikas] [建立了一个伟大的系统](https://hackaday.io/project/11834-pc-imobilizer)，远程输入按键锁定他的屏幕，或者用他的密码解锁。一个现成的 433 MHz 密钥卡连接到一个 Arduino micro，模拟连接到他的计算机的键盘。这个系统很简单，但是效果很好。(参见下面的视频演示。)

但是作为一个安全设备，它是可怕的。在易贝可以买到的一些 el-cheapo 密钥卡不使用滚动码——任何拥有类似密钥卡接收器的人都可以监听传输，设置一些 DIP 开关，并轻松地重放它。即使它确实使用了滚动码，如果你办公室里的任何人玩 RTL-SDRs(T1)，你可能仍然在向每个人广播你的密码。

第二个故障点是[Matikas]的密码存储在 Arduino 上的 EEPROM 中。这比写在键盘下的便利贴上要好一点，但不是针对 AVR 程序员的对手。当他喝第一口咖啡时，我们已经登录了，他正在买啤酒。

撇开安全性不谈，这很有趣，而且用汽车遥控器锁定和解锁你的电脑也很酷。我们确信这是正确的态度。有时候乐趣比偏执更有趣。但如果你在像马蒂亚斯这样的办公室工作，可能就不会了。

 [https://www.youtube.com/embed/fcAAZejl6nY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/fcAAZejl6nY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

