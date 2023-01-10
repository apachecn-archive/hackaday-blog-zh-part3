# 面板仪表到蓝牙黑客劫持显示段

> 原文：<https://hackaday.com/2016/09/21/panel-meter-to-bluetooth-hack-hijacks-the-display-segments/>

网上有大量价格低廉的数字仪表模块。电流、电压、频率或它们的组合都可以是你的，只需要几美元和等待发货。不幸的是，尽管这些仪表都是独立的单元。它们没有串行端口或其他接口来记录它们的读数。

不过，这次失败并不是(斯科特·哈登)的障碍。他只是通过使用 ATmega328 微控制器来捕捉发送到模块显示 led 的信号，并将其解释为蓝牙模块的读数，从而为他的组合式电压和电流表模块添加了蓝牙接口。他详细介绍了仪表逆向工程的过程和他的构建。结果是一堆有趣的电线，末端挂着一个 DIP ATmega。但是它出色地完成了要求它完成的任务，当它被安装在一个项目箱中时，你不知道里面藏着什么。

他已经在他的 GitHub 库中提供了他的项目代码[，我们可以看到这对于其他类似的显示来说是一个很有价值的技术。在休息时间下面的视频中，他给了我们一个完整的总结，好像他的综合报道还不够。](https://github.com/swharden/AVR-projects/tree/master/ATMega328%202016-09-15%20CVM)

 [https://www.youtube.com/embed/fp7uuyBCSvI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/fp7uuyBCSvI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[Scott]是一个多产的黑客，他的作品我们已经在这些页面上介绍过几次了。最近我们有了他的 [PC 频率计数器](http://hackaday.com/2016/09/09/very-simple-pc-frequency-counter-works-up-to-100mhz/)，但是我们已经看到了他的其他几个项目是他的[用于老年计数器的 USB 接口](http://hackaday.com/2011/07/25/adding-usb-connectivity-to-old-benchtop-tools/)，和他的[单片 Hellschreiber 发射器](http://hackaday.com/2011/08/08/scott-made-a-single-chip-hellschreiber-on-earth/)。