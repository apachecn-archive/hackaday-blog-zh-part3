# 机器人:执行我的命令！

> 原文：<https://hackaday.com/2017/07/11/robot-do-my-bidding/>

遥控机器人并不是什么新鲜事。使用蓝牙也不是那么不寻常。[sayantan 4]所做的是让[成为一个蓝牙机器人，通过他的手机接受语音命令](http://www.instructables.com/id/Voice-Controlled-Bluetooth-Car/)。这个机器人本身并不出色。Arduino 和 HC05 模块构成了大部分电子设备。一个标准的马达驱动器驱动两个轮子。

Arduino 通常不做太多的语音处理，诀窍当然是在电话应用程序中。[用于 Arduino](https://play.google.com/store/apps/details?id=robotspace.simplelabs.amr_voice&hl=en) 的 BT 语音控制是一款免费下载软件，只需通过蓝牙向主机发送字符串。如果你对着手机说“你好”,机器人就会接收到`*Hello#`,任何能接收蓝牙数据的电脑都可以处理这个字符串。

当然，这不一定是机器人，尽管程序描述反复提到机器人。例如，你可以很容易地用它给自制的家庭自动化系统添加语音命令。不管应用程序的名字是什么，你是否真的有 Arduino 在另一端取决于你。

如果你想在不发送数据给某个邪恶的霸主并且依赖手机的情况下进行语音控制，你可以看看 [MOVI 板](https://hackaday.com/2016/12/11/arduino-clock-is-hal-1000/)。当然，那个项目是一个时钟，但是我们以前也见过[声控机器人](https://hackaday.com/2015/05/07/sparc-a-voice-controlled-robot/)。