# 午餐钱的手势控制

> 原文：<https://hackaday.com/2017/12/03/gesture-control-for-lunch-money/>

[Dimitris Platis]想在他的电脑上添加手势控制。你可能会认为这很昂贵，但通过结合一个小型的 Arduino、一个带手势控制器的分线板和一个互连 PCB，他成功地以大约 7 美元的价格实现了它。这不包括可选的 [3D 打印外壳](https://www.tinkercad.com/things/h5ymCb1lX3J)，我们认为如果你不介意一些电线和进一步削减成本，你可以省略互连板。[Dimitris]称之为 Nevma，你可以在下面的视频中看到该设备的工作原理。

该项目的核心是一个测量光线和运动的传感器。如果你从中国订购，芯片和分线板只需几美元。如果你不介意多花一点钱，你可以在美国找到它们。该设备有一个 I2C 接口，并且[Dimitris]使用一个微型的 SS Micro 作为 USB 接口和 CPU。

传感器芯片是为手机市场制造的，也可以感知接近度。根据其数据表:

> 手势检测利用四个方向光电二极管来检测反射的红外能量……手势引擎的架构具有自动激活(基于邻近引擎结果)、环境光减法、串扰消除、双通道 8 位数据转换器、省电转换间延迟、32 数据集 FIFO 和中断驱动的 I2C 通信。

几块钱就有这么大的能量。Sparkfun 有一个[库](https://github.com/sparkfun/SparkFun_APDS-9960_Sensor_Arduino_Library/tree/V_1.4.2)(和一个匹配板)【Dimitris】使用它。该库作为 beerware 发布。特别是，文档中说:“代码是 beerware 如果你在当地看到我(或任何其他 SparkFun 员工)，并且你发现我们的准则很有帮助，请给我们买一轮！”

我们真的很喜欢 Nevma。你不需要将任何设备握在手中。它看起来也比我们见过的使用[声纳](https://hackaday.com/2017/11/01/listening-for-hand-gestures/)的解决方案(甚至是[创造的](https://hackaday.com/2015/10/07/bootstrapping-motion-input-with-cheap-components/))更圆滑。

 [https://www.youtube.com/embed/ge5iq_UEvFM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ge5iq_UEvFM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

