# 你在床上吗？

> 原文：<https://hackaday.com/2016/04/17/are-you-in-bed/>

如果你正在建立一个无所不知的家庭自动化系统，它的决策能力取决于你给它的输入。[彼得威尔]自制的全景监狱[现在知道什么时候有人在床上](https://www.openhardware.io/view/65/Bed-Occupancy-Sensor)。这样，[彼得威尔]的自动百叶窗就不会在他周末睡懒觉时打开。

[彼得威尔]没有走捷径。(在我们看来，那应该是床脚下面的一个重量传感器。)相反，他的系统更加灵活，建立在电容传感的基础上。他试过床垫下的力传感器和压电传感器，但没有一个像电容那样可靠。床垫下的铜带网充当天线。

细节由 Microchip 的 MPR121 处理。Arduino 和 nRF24L01+模块完善了构建。视频中有一些关于使用电容感应芯片的提示(见下图)，他的网站上有 Arduino 代码。

电容式感应的优势在于，您可以轻松定义想要覆盖的区域，只需将胶带放在您想要的位置即可。这样，你就可以根据床的哪一侧被占用来建立不同的规则。

因此，在你的床上添加电容传感器，把你复杂得离谱的家庭自动化系统推向疯狂的边缘！

 [https://www.youtube.com/embed/KofnH0reWCQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/KofnH0reWCQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

