# 松弛，向后兼容 1982 年

> 原文：<https://hackaday.com/2016/11/29/slack-backwards-compatible-with-1982/>

Slack 很棒，但是当前的实现存在一些小问题。没有 Palm 的客户端，没有 Newton 的客户端，也没有 Commodore 64 的客户端。最近，杰夫·哈里斯(Jeff Harris)修复了这些严重的疏忽。他在 6502 汇编中为 Commodore 64 构建了一个本地 Slack 客户端。

当处理网络应用程序和 C64 时，首先想到的问题是如何与外界对话。有 C64 网卡和 ESP 加密狗，但对于这个版本[Jeff]转向 C64 [用户端口](https://www.c64-wiki.com/index.php/User_Port)。这种串行和并行端口的卡边缘组合允许 C64 与任何具有 RS-232 的东西对话，并且通过简单的适配器，[Jeff]让他的旧计算机与连接到互联网的 Raspberry Pi 对话。

C64 Slack 客户端本身是用 6502 汇编编写的，拥有你所期望的一切特性。但是，Pi 需要与 Slack API 对话，并使用 NodeJS 应用程序将 C64 中的位翻译成 API 可以理解的内容。

有用吗？当然了。Slack 毕竟只是文本，这里似乎没有任何 PETSCII 的古怪。你可以看看下面的视频。

 [https://www.youtube.com/embed/aIuSKUNrR6o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/aIuSKUNrR6o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

