# 恶意、节俭和负担得起的逻辑分析仪的优点

> 原文：<https://hackaday.com/2018/01/03/spite-thrift-and-the-virtues-of-an-affordable-logic-analyzer/>

Perl 之父[拉里·沃尔]列出了所有程序员的三大美德:懒惰、急躁和狂妄。在看到 Saleae 将他们流行的逻辑分析仪的价格抬高到可笑的水平后，[CNLohr]增加了第四个优点:恶意。由于他在过去几天用 Cypress FX3 进行的测试可能会导致一个非常便宜的 DIY 逻辑分析仪，我们可能很快就能增加另一个优点:节俭。

故事开始于一两年前，当时[CNLohr]以 45 美元的价格获得了一个 Cypress FX3 开发板。由于缺少 Windows 系统的机器，这块板一直闲置着，但在看到我们最近关于基于 FX2 的极简逻辑分析仪[的文章后，他开始摆弄这块板，看看它是否能点燃他对 Saleae 的仇恨。FX3 是一个简洁的小芯片，具有 100 MHz 通用可编程接口(GPIF)总线，基本上让它像一个易于使用的 FPGA 一样工作。](http://hackaday.com/2017/12/22/logic-analyzer-pushes-the-limits-of-miniaturization/)

他准备在这个项目上花几个月的时间，但他惊讶地在几天内就在恶意节俭的任务上取得了重大进展，以每秒 200 多兆字节的速度从 GPIF 中读取 16 位，并通过 USB 3.0 端口将其转储。[Charles]“FX3 的库为许多很酷的东西奠定了基础，从逻辑分析仪到 SDR 等等——现在只需要有人来构建它们。

当然，寻找便宜但功能强大的逻辑分析仪并不是什么新鲜事。去年，[【珍妮名单】](https://hackaday.com/2016/10/26/an-open-source-96-msps-logic-analyzer-for-22/)和[【比尔牛群】](https://hackaday.com/2016/12/13/compiling-a-22-analyzer/)都将 22 美元的冰棍视为潜在的 Saleae 搅拌器。

 [https://www.youtube.com/embed/_LnZrXrdC00?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/_LnZrXrdC00?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢【themreadbeard】2018 第二条提示。