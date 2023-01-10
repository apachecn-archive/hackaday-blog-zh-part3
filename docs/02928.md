# 建立自己的无刷电机

> 原文：<https://hackaday.com/2016/07/13/build-your-own-brushless-motor/>

对许多初露头角的科学爱好者来说，用一卷电线、一些磁铁和一些回形针制造一台电动机是一项必经之路。这些电机是简单的有刷电机。也就是说，电磁体向永磁体旋转，旋转断开电路，允许电磁体依靠惯性继续旋转。最终，连接再次完成，循环重新开始。真正的有刷电机对 DC 供电电流进行整流，使得电磁铁在中途改变极性。无论哪种方式，基本设计都是在外部(静止部分)安装永久磁铁，在内部(旋转部分)安装电磁铁。

无刷电机翻转这个里面。旋转部分(转子)有一个永久磁铁。固定部分(定子)有多个电磁铁。通过控制电磁铁，转子旋转。由于没有电刷，这些电机通常效率更高，它们不会产生太多的电噪声，也没有电刷磨损的危险。此外，电磁体保持不动使电机更容易接线，如果需要，更容易冷却电磁体。工作原理类似于步进电机。步进机通常针对小的精确步进进行优化。无刷电机针对旋转而非步进进行了优化。

[Axbm]用 PVC 管、一些磁铁、电线和铁棒制造了一个巧妙的无刷马达。计划很简单:建造一个 PVC 框架，用 PVC 和磁铁建造一个转子，并在框架上安装电磁铁。一个 Arduino 和一些 fet 驱动线圈，尽管您可以使用任何方法驱动电机。你可以在下面的视频中看到整个过程。

一个有趣的花絮是线圈的缠绕。【Axbm】在每个铁芯上绕 600 匝线(软铁最好，虽然也可以用不锈钢，更好找)。完成后，他没有剪断电线，而是继续缠绕下一块磁铁。为了保持磁场的正确方向，一个磁体的绕组必须与前一个绕组的方向相反。所以如果你顺时针缠绕一块磁铁，下一块磁铁一定是逆时针的。

我们已经看到其他[无刷电机](https://hackaday.com/2016/04/10/make-a-bldc-motor-from-scraps-you-can-find-in-the-garage/)建立。我们也报道了更多的[老练的司机](https://hackaday.com/2014/10/08/brushless-motor-controller-shield-for-arduino/)。

 [https://www.youtube.com/embed/kYdZ_WnODi4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/kYdZ_WnODi4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

