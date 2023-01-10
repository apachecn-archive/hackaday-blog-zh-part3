# Numato Opsis:基于 FPGA 的开放式视频平台

> 原文：<https://hackaday.com/2015/10/02/numato-opsis-fpga-based-open-video-platform/>

想象一下，你正在主持一个会议，你想做一个专业的工作，记录发言者和他们的甲板。您需要从演示者的笔记本电脑上录制一个视频流，用相机拍摄演示者的另一个视频流也不错。但是你还需要将演示者的屏幕显示在一两台投影仪上，供现场观众观看。也许你想把所有这些都转储到你的电脑上，这样你就可以同时存档演示文稿，并通过互联网把它流传出去。

这正是 [hdmi2usb 项目](http://hdmi2usb.tv/home/)试图在开源软件惯例的软件方面解决的问题。为了配合这个软件，[蒂姆·安塞尔]已经建造了[Numato Opsis FPGA 视频板](https://www.crowdsupply.com/numato-lab/opsis)，将一切联系在一起。该平台的伟大之处在于硬件[和固件](https://hackaday.io/project/7772-numato-opsis-fpga-based-open-video-platform)[也都是开源的。](https://hackaday.io/project/7774-hdmi2usbtv-open-video-capture-hardware-firmware)

因为一切都是开放的，板上有 FPGA 进行视频处理，所以你基本上可以自由地处理传输中的内容，所以它可以作为 FPGA 视频实验板。看起来他们也打算移植代码，这样 Opsis 就可以取代停产但仍然开源的 Milkimist One 视频效果平台。

这个设计非常可爱的一点是，它通过 USB 作为摄像头进行报告，所以你可以在任何类型的计算机上录制视频，而无需安装额外的驱动程序。总而言之，这是一场 FPGA 视频盛宴，背后有一堆开源软件支持。令人印象深刻，[蒂姆]！