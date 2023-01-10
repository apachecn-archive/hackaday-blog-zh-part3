# 莫尔斯电码闪烁珠宝

> 原文：<https://hackaday.com/2018/05/06/morse-code-blinking-jewelry/>

随着如今电子零件和电池的尺寸，非常小的物品显然变得越来越可行。[Yann Guidon]使用最少的表面贴装元件和一个小型锂离子电池制作了一些令人惊叹的 LED 珠宝。为了让珠宝更加突出，而不仅仅是闪烁，这些发光二极管会以[莫尔斯电码](https://en.wikipedia.org/wiki/Morse_code)闪烁一条短消息。

这是对[Yann]几年前所做的一些工作的更新和开源，迭代产生了一个更小的设计。但最新版本的主要部分是使用一个小的微控制器增加了莫尔斯电码闪烁。所用的微控制器[Yann]是 PIC10F200 的 SMD 版本，一种小型 8 引脚 PIC 微控制器。一个电阻和一个金属夹焊接在 Luxeon Star LED 的焊盘上。led 是欠电压的，所以它们不太亮，所以散热器不是真的需要，但它对元件来说是一个很好的尺寸。因为 LED 不会产生太多热量，所以 LED 所在的铝框架的背面被刻出一点，以便小型锂离子电池可以放在那里。

最后的组件是代码本身，Yann 已经把它作为一个汇编文件发布了。相关的文本文件包含您希望耳环闪烁的消息的文本。该文本文件最多可包含 190 个字节。shell 脚本将文本转换为可以包含在 asm 文件中的文件。该脚本运行后，汇编代码并将其闪存到 PIC 中，这样就完成了！

我们已经看到了一些其他的 LED 珠宝项目，包括[这个 LED 订婚戒指](https://hackaday.com/2013/05/20/adding-leds-to-an-engagement-ring/)和[这些小小的发光耳环](https://hackaday.com/2017/02/12/tiny-led-earrings-are-a-miniaturization-tour-de-force/)。你可以在下面的视频中看到【Yann】的项目视频:

 [https://www.youtube.com/embed/9EwlCHsH_cs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/9EwlCHsH_cs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2018](https://hackaday.io/prize) is Sponsored by: [![Microchip](img/20eb9d92b47da4c15177567c02a65727.png)](https://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey)  [![Supplyframe](img/2d012d9fc9c7873688699aeadb4742d2.png)](https://supplyframe.com/)