# ESP32 让不太智能的灯变得智能

> 原文：<https://hackaday.com/2018/01/11/esp32-makes-not-so-smart-lights-smart/>

长久以来被认为是理所当然的——灯是现代生活的基本必需品。从第一个灯泡出现的时候起，我们就可以不用火在黑暗中行走。随着物联网的出现，在给自己贴上硬件黑客的标签之前，有点智能已经成为一种要求。有许多方法可以做到这一点；最常见的一种是使用 ESP32。[Luca Dentella]在某种程度上是一位 ESP32 专家，他写了一篇关于如何使用该芯片的精彩教程。该教程旨在制作一组可通过智能手机网络浏览器控制的灯[以及一个光强传感器。](http://www.lucadentella.it/en/2018/01/08/esp32lights/)

现在，在你把这当成简单的工作之前，请考虑以下几点。他使用 Lolin32 lite 开发板、BH1750 光强传感器和继电器来连接灯光电源。他编写了自己的固件，并深入研究了开发 HTTP 接口和将代码刷新到正确内存的具体细节。

我们在 Hackaday 已经看到了很多 ESP32 项目，包括这个最有趣的[时钟](https://hackaday.com/2017/11/27/over-engineered-clock-uses-no-less-than-five-esp32s/)。请务必观看下面的视频，了解智能灯的使用情况。

 [https://www.youtube.com/embed/56xeacghJrc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/56xeacghJrc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

