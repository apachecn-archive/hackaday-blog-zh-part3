# 微软从微控制器开始保护物联网

> 原文：<https://hackaday.com/2018/04/25/microsoft-secures-iot-from-the-microcontroller-up/>

对无安全保障的物联网设备过剩感到沮丧？微软也是。他们使用定制的 Linux 和硬件来解决这个问题。

微软[宣布了一个名为“Azure Sphere”的安全物联网设备新生态系统](https://azure.microsoft.com/en-us/blog/introducing-microsoft-azure-sphere-secure-and-power-the-intelligent-edge/)这个系统有三层:硬件、软件和云。硬件组件是微软认证的微控制器，其中包含微软 Pluton，这是一个硬件安全子系统。首款微软认证的 Azure Sphere 芯片将是今年推出的[联发科 MT3620](https://www.mediatek.com/products/azureSphere/mt3620) 。软件层是一个定制的基于 Linux 的操作系统(OS)，比低功耗物联网设备常见的普通实时操作系统(RTOS)功能更强。是的，没错。微软正在发布一款默认内置 Linux 的产品(与[Linux 的 Windows 子系统](https://hackaday.com/2016/03/30/windows-and-ubuntu-cygwin-can-suck-it/)相对)。最后，云端层被称为“交钥匙”解决方案，它使基于云的功能(如更新、故障报告和身份验证)更加简单。

 [https://www.youtube.com/embed/iiDF26HNh-Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/iiDF26HNh-Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



就复杂性而言，这似乎类似于[微软的物联网核心产品](https://developer.microsoft.com/en-us/windows/iot),[可以在树莓 Pi 上运行，但旨在使用 Windows API](https://hackaday.com/2015/08/13/raspberry-pi-and-windows-10-iot-core-a-huge-letdown/)构建单一用途的设备。与专业云服务的协调可能会使这超出一般制造商的标准工具包，但任何希望投入生产的人都应该尝试从这个系统中学习，因为它似乎旨在减少物联网设备似乎难以解决的安全和更新问题。微软也[出版了该项目的简史](https://www.microsoft.com/en-us/research/blog/from-research-idea-to-research-powered-product-behind-the-scenes-with-azure-sphere/)。

你会用安全的物联网系统构建什么？我们希望像这样的安全物联网设备将会激增，不像英特尔的[停产](https://software.intel.com/en-us/iot/hardware/discontinued) [爱迪生](https://hackaday.com/2014/09/10/hands-on-with-the-intel-edison/)和[伽利略](https://hackaday.com/2017/06/19/intel-discontinues-joule-galileo-and-edison-product-lines/)，以及英特尔驱动的 [Arduino 101 板](https://hackaday.com/2017/07/25/the-end-of-arduino-101-intel-leaves-maker-market/)。

感谢[RQDQ]和[RoGeorge]！