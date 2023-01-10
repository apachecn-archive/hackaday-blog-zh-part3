# 与 Macintosh Classic 更好地联网

> 原文：<https://hackaday.com/2015/12/15/better-networking-with-a-macintosh-classic/>

尽管情况可能不再如此，但如果你比较一下 1990 年的 Mac 和 PC，你会发现 Mac 遥遥领先。个人电脑饱受 DOS 之苦，而苹果电脑却喜欢真正的非位图字体。Windows PC 需要 LANMAN 连接到网络，而 Mac 将网络内置到每台机器中。事实上，过去的任何 Mac 都可以使用这种内置网络连接到互联网，但大多数旧的 Mac 网络黑客都依赖于 PPP 或其他网络串行转换。[Pierre]认为在互联网上安装旧的 Mac 是不完整的理解，并决定用苹果的内置网络将 Mac Classic 连接到互联网。

从第一台 Macintosh 开始，Apple 就包含了一个简单的网络协议，允许用户通过局域网共享硬盘、文件夹和打印机。这种网络设置被称为本地通话。它并不意味着互联网或非常大的网络；计算机之间的连接基本上是菊花链串行电缆和后来的 RJ-11(电话)电缆。

LocalTalk 存在了很长一段时间，即使是现在，如果你需要用上世纪制造的 Mac 做任何事情，它也是文件传输的最佳选择。由于 LocalTalk 的长寿，路由器和 LocalTalk 到以太网适配器可以很容易地找到。唯一的问题是找到一种既能说 TCP/IP 又能说 LocalTalk 的现代设备。你不能用新的 Mac 来做这件事；自从雪豹事件后，本地话就在 OS X 消失了。不过，你可以用覆盆子酱来做。

稍微摆弄一下 MacTCP 和其他一些 1993 年左右的软件，[Pierre]甚至可以在网上找到他的旧 Mac Classic。当然，这些浏览器都已经过时了(使得 Hackaday 复古版非常有用)，但是[Pierre]能够加载 rotten.com。使用 8MHz 的 CPU 和 4MB 的 RAM 需要一段时间，但它确实完成了工作。

你可以看看下面[Pierre]的演示视频。

 [https://www.youtube.com/embed/JAGLS1e8KCI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/JAGLS1e8KCI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

