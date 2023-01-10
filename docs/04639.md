# OWL 不安全的能源监控网络

> 原文：<https://hackaday.com/2017/01/02/owl-insecure-internet-of-energy-monitors/>

[Chet]从 OWL 买了一个电力监视器，特别是因为它是开放的，很容易在他的家庭网络范围内对他进行黑客攻击。耶！不幸的是， [~~在他的家庭网络之外也很容易黑掉~~的阅读器](http://www.chet.ie/?p=267)，这是由于看起来非常草率的安全措施。

该安全漏洞的简短版本是， [OWL 能源监视器](http://www.theowl.com/)似乎正在向 OWL 的服务器发送数据，然后这些数据可以通过普通 HTTP(不是 HTTPS)和以下 API 访问:`[http://beta.owlintuition.com/api/electricity/history_overview.php?user=&nowl=&clientdate=](http://beta.owlintuition.com/api/electricity/history_overview.php?user=&nowl=&clientdate=)`。还不错，对吧？他们需要用户名和密码，以及设备的 ID 号。也许有人可以拦截你的请求，远程读取你的电表，因为它没有加密交易？

没有。糟糕多了。[Chet]发现用户名和密码字段似乎没有被检查，ID 号是设备的 MAC 地址，这使得很容易猜测其他设备 ID。[Chet]尝试了 256 台 MAC，得到了 122 个有效数据的响应。我的天啊。

以此作为友好的提醒和警示。如果你正在运行任何物联网设备，可能值得听听他们在说什么，并记下他们对谁说的，因为每次你将数据发送到“云”时，你都在相信其他人已经做了功课。他们将拥有的并不是一个既定事实。