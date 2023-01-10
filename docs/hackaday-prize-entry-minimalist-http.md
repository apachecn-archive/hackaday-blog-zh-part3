# Hackaday 奖参赛作品:极简主义 HTTP

> 原文：<https://hackaday.com/2017/07/23/hackaday-prize-entry-minimalist-http/>

对于他的 Hackaday 奖参赛作品，[Yann]正在建造一些不是硬件的东西，但它仍然很迷人。他提出了一种用 c 语言编写的极简 HTTP 兼容服务器。它很小，可移植，在某些情况下，这将是比将完整的 Linux 堆栈放入单个传感器更好的解决方案。

这个微型 HTTP 服务器有两个核心模块，每个模块都有特定的用途。文件服务器完全按照它在 tin 上所说的做，但是 HTTaP 更有趣一些。HTTaP 是 2014 年首次发布的协议[，旨在成为 WebSockets 的更简单替代方案。](http://connect.ed-diamond.com/GNU-Linux-Magazine/GLMF-173/HTTaP-Un-protocole-de-controle-base-sur-HTTP)

【Yann】一直在试验 HTTaP，[而且好处很明显](https://hackaday.io/project/20170-httap)。你不需要 Apache 来利用它，HTTaP 可以直接处理 HTML/JavaScript 页面，只使用 GET 和 POST 消息，你就可以控制硬件和逻辑电路。

由于这是一个最低限度的 HTTP 服务器，安全性是可疑的。不过，这不是重点。这只是一个设计用于实验室或有空气间隙的受控环境的工具。安全、调度、加密和认证不是 HTTP 或这个微型 HTTP 服务器的一部分。

The [HackadayPrize2017](https://hackaday.io/prize) is Sponsored by:[![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Texas Instruments](img/3734f1c96ffff85ea2a7eaddc92844ba.png)](https://hackaday.io/ti)