# 焊接更多的 USB 端口到树莓派零

> 原文：<https://hackaday.com/2015/12/12/solder-more-usb-ports-to-the-raspberry-pi-zero/>

慢慢地，树莓派的零数正落入每个想要一个的人手中。但是很快，人们意识到一个 USB 端口是不够的，只有一个 USB OTG 端口是最经济的解决方案。Pi Zero 的背面确实有很多测试点，而[Peter van der Walt] [足够聪明，可以拿出一个 4 端口集线器，你可以直接焊接到 Pi Zero](https://openhardwarecoza.wordpress.com/2015/12/07/raspberry-pi-zero-4-port-usb-hub-open-source-pcb-design/) 。

[Peter]对 Pi 上的 USB 端口有一定的经验，在这个便宜又奇妙的电路板底部提供的测试点提供了将单个 USB OTG 端口连接到 USB 集线器所需的一切。[我们以前在](http://hackaday.com/2015/12/03/4-port-usb-raspberry-pi-zero-piggy-back-hack/)中见过这样的情况，在 Zero 和现成的 USB 集线器之间有一些脆弱的焊接连接。[Peter]的构建是通过这些测试点将 USB 集线器直接焊接到 Pi 上来实现的。这是第一个专门为给 Pi 提供四个 USB 端口而设计的硬件，同时只使它变得更厚。

[Peter]用于构建的芯片是 TI tusb 2046 b，这是一种将单个 USB 端口变成 4 端口集线器的设备。这是一个数量上只需要大约 2 美元的零件，如果你想建造一千个这样的可焊接 USB 集线器，USB 连接器本身只需要大约 0.60 美元。现在你明白为什么 Pi 基金会没有在 Pi Zero 上包括一整套端口，但这确实意味着当它不可避免地在中国被克隆时，你应该能够以低于 10 美元的价格买到这个板。

[Peter]还没有让这块板工作。事实上，他刚刚把格柏送去 PCB 工厂。一旦[彼得]拿回电路板并焊接上微小但可忍受的 0603 零件，就会有更新。