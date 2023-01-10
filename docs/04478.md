# [欢]解放路由器

> 原文：<https://hackaday.com/2016/12/16/haun-liberates-a-router/>

[Huan Truong]得到了一个 WiFi 路由器，他想通过在上面安装免费固件来改进它。不幸的是，问题中的路由器有点旧，而且从一开始就不流行，这意味着它不被通常的开放固件所支持。问题是它只有一个 4 MB 的闪存，但[欢]决心让它工作。(剧透:[他做到了，并且完整记录了](https://cdn.ampproject.org/c/www.tnhh.net/mobile/posts/lede-on-wnr2000v1-unsupported-hardware.html)。)

闪存解决方案基本上包括重新划分空间，然后告诉 [u-boot](http://www.denx.de/wiki/U-Boot/) 在哪里可以找到所有东西。在像[Huan]拥有的 WNR2000 这样的路由器上，闪存是内存映射的，这意味着向闪存起始位置(`0xbf000000`而不是`0x00000000`)添加一个偏移量，并记住始终这样做，以便他不会覆盖 MAC 地址等内容。

[欢]使用了 [OpenWRT](https://openwrt.org/) 的 [LEDE fork](https://lede-project.org/) ，并从源代码中重新构建了它，因为他需要一个小版本来适应他有限的闪存。随着这项任务的完成，它的工作。完成了吗？不，【欢】然后提交了一个[拉请求](https://github.com/lede-project/source/pull/611)给乐的，现在你不用复制就可以享受他的劳动成果了。但是，如果你有另一个低闪速、不引人注意的路由器，你就已经开始使用 LEDE 了。

路由器可能是我们在这里看到的被黑客攻击最多的设备，如果有合适的固件，它们可以变得非常有用。有时候运行一个定制的固件相对容易，就像这里一样，有时候它需要一些[深度逆向工程](http://hackaday.com/2016/12/14/tp-link-debug-protocol-give-up-keys-to-kingdom/)。但是保持你的路由器黑客印章是好的，因为他们[可能不总是像他们现在](http://hackaday.com/2016/02/26/fcc-locks-down-router-firmware/)一样开放。