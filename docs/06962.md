# 超声波阵列快速廉价地获得距离数据

> 原文：<https://hackaday.com/2017/08/30/ultrasonic-array-gets-range-data-fast-and-cheap/>

你的平行停车怎么样？这是一个许多司机害怕到避之不及的场景。但是这种 360 度超声波传感器会让最熟练的司机感到羞愧，至少是那些驾驶微型遥控汽车的司机。

多看几遍下面的视频，你会发现在测试系统的限制下，[Dimitris Platis]“sonic disc”传感器在解决平行泊车问题方面做得非常好，这是一种非常罕见的驾驶技术，汽车公司已经花了数百万美元来开发为你做这件事的车辆。基本任务是良好的空间关系，这就是 SonicDisc 的用武之地。八个 HC-SR04 超声波传感器的环形阵列连接到 ATmega328P，SonicDisc 利用中断来尽可能快地读取八个传感器。该阵列可以每 10 毫秒读取一组完整的读数，这足够快，可以对连续的读数进行平均，以过滤掉一些返回的噪声。通过 I2C 与汽车的微控制器交谈，传感器提供了丰富的测距数据，让汽车快速完成平行泊车动作。另外，SonicDisc 是开源的，构建起来也很便宜——大约 10 美元一份。

宁愿用光来获得你的范围数据？目前市场上有一些非常便宜的激光雷达设备。

 [https://www.youtube.com/embed/V4oNjup3uh4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/V4oNjup3uh4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/EGXUQHS0aXI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/EGXUQHS0aXI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[通过 [r/Arduino](https://www.reddit.com/r/arduino/comments/6wlll4/sonicdisc_a_360_ultrasonic_scanner_that_costs_10/)