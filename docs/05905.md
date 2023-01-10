# Javascript 艺术在 URL 中

> 原文：<https://hackaday.com/2017/05/13/javascript-art-is-in-the-url/>

[Alexander Reben]创造了技术艺术，现在他鼓励你也这样做——在 URL 内[。噱头？使代码足够小以适合链路的数据部分。为了帮助解决这个问题，他建立了一个网页，](https://www.4qr.xyz/)[从 URL 中解压缩并包装代码](https://www.4qr.xyz/reference/)，然后动态地将其插入 HTML。他的网站实际上应用或取消了 URL 中 JS 缩小的所有技巧，并将其转化为内容。

例如，`[https://4QR.xyz/c/?eJzzSM3JyVcIzy_KSVEEABxJBD4](https://4QR.xyz/c/?eJzzSM3JyVcIzy_KSVEEABxJBD4)`解压缩到一个网页，上面写着“Hello World！”。但当你开始用 Javascript 或 HTML5 编写“艺术”代码时，乐趣才真正开始。现在在[画廊](https://www.4qr.xyz/gallery/)有几个例子，但是【亚历山大】希望你贡献你自己的。横幅来自[这个链接](https://4qr.xyz/dw/?eJwVjMsKwjAQAL9G2DxMYxsrS8w_CB68CbXGdqO0kCzo59uchoFhRvOlJ8_3YP1rzUABPZ3b2HlSoRUldA2gOeyBFTWIYodC_8wjTrRcBp5B6BRIntQVSDrFG1nU4kNLvNVxKLJsPuQRsLf66Kwu0qFOOinT17RwXt8RxB_F-CeR)。

我们觉得在链接中不透明地传递 JS 代码有些可疑，但是由于 URL 在[Alexander]的服务器上解码，我们还没有看到[XSS 攻击](http://hackaday.com/2016/03/23/the-dark-arts-cross-site-scripting/)。如果你能发现这个设置的安全问题，或者更好的是如果你写了一个漂亮的动画，请在评论中告诉我们。