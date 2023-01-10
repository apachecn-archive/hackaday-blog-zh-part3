# 斗杆通过反作用轮保持自身平衡

> 原文：<https://hackaday.com/2016/08/11/stick-balances-itself-with-reaction-wheels/>

倒立摆是一个非常经典的动力学问题，反作用轮很酷。这就是为什么我们喜欢[Mike Rouleau]的[自动平衡杆。](https://www.youtube.com/watch?v=woCdjbsjbPg)

这段视频在休息后可以观看，细节相当少，但他在评论中提供了一些细节。顶部的小黑盒是 GY-521 陀螺仪模块。它将数据发送到一个 Arduino，这个 Arduino 连接到屏幕上的黑色电线上。Arduino 进行数学运算，然后使用电机控制器以正确的速度驱动[反作用轮](https://www.ethz.ch/en/news-and-events/eth-news/news/2016/07/high-speed-motor-for-satellites.html)。


[Mike]提到他没有对演示的动态模型做任何太花哨的事情。他甚至手动调整 PID 值，而不是诉诸更花哨的训练方法。Arduino 只需运行一点代码，并可选地将一些数据流回计算机进行可视化。

这根棍子可以坚持到停电，这是一个非常酷的演示。正如一些人在评论中提到的那样；这会是一个吸引人的书桌装饰品。

 [https://www.youtube.com/embed/woCdjbsjbPg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/woCdjbsjbPg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

