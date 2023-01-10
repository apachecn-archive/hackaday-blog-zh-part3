# 虚拟现实中模拟的 N64 让 Hyrule 走向 3D

> 原文：<https://hackaday.com/2018/07/10/n64-emulated-in-vr-makes-hyrule-go-3d/>

任天堂 64 有一些突破性的和受欢迎的 3D 游戏，并且[Avaer Kazmer]认为只需篡改一些东西就足以欺骗模拟器在 VR 中播放*时间的陶笛*，完成立体 3D。结果不仅仅是在虚拟现实中的模拟屏幕上运行仿真器；该软件正确地将 Hyrule 世界的略微不同的视角呈现给每只眼睛，以便以原始版本永远无法实现的方式真正实现 3D 效果，并在此过程中使用 VR 控制器进行播放。VR 模拟器解决方案名为 [Emukit](https://github.com/webmixedreality/emukit#emukit-mixed-reality-emulator) ，与 [Exokit](https://github.com/webmixedreality/exokit#exokit-browser) 配合使用效果最佳，后者是一款用于 AR 和 VR 环境的 JavaScript web 浏览器，[Avaer]是其开发者。

事实证明，有一些挑战需要解决，也有一些新的问题需要解决，尤其是映射 VR 控制器以合理的方式控制 N64 游戏。有一件事是不可避免的，N64 的渲染世界现在可能会在 3D 中弹出，但它仍然是从一个矩形的舞台上跳出来的。毕竟，N64 仍然只是在电视屏幕大小的部分呈现一个世界；矩形窗口之外的任何东西实际上都不存在，只要模拟 N64 在运行，就没有办法绕过它。尽管如此，结果还是令人印象深刻，下面嵌入了一个视频演示，您可以亲自查看效果。

 [https://www.youtube.com/embed/_yQCjKuRRl0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/_yQCjKuRRl0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



N64 黑客通常以将硬件[变成时尚的便携式系统](https://hackaday.com/2015/07/19/a-beautifully-crafted-n64-portable/)的形式出现，但愚弄一个 N64 仿真器在 VR 中渲染？这是一个非常巧妙的把戏。