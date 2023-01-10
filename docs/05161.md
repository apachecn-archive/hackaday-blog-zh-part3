# 醒醒！猫回来了！

> 原文：<https://hackaday.com/2017/03/05/wake-up-the-cat-came-back/>

为了最大限度地利用连接到微控制器的电池，你可能需要让它进入睡眠状态，越深越好。[Rgrokett]对他的猫的夜间习惯很好奇，想出了一个[好的小窍门来延长他正在使用的 ESP8266 的电池寿命](https://github.com/rgrokett/ESP8266_PIRv2)。

[rgrokett]的猫通过猫门进出。他认为当门周围有动静时，PIR 传感器会让他知道。然后他就可以知道那只猫是否在附近。让 PIR 传感器和 ESP8266 微控制器(一个 Adafruit Huzzah)一直开着会很快耗尽电池，所以[rgrokett]决定尝试让 Huzzah 休眠。

这个版本的诀窍在于，PIR 传感器用于在触发时重置 Huzzah。Huzzah 要求复位开关从高电平变为低电平，但 PIR 触发器从低电平变为高电平，因此使用晶体管来反转 PIR 传感器的触发信号。当 Huzzah 醒来时，它连接到 WiFi 网络，并通过 IFTTT 向[rgrokett]发送电子邮件([rgrokett]的描述介绍了建立与 IFTTT 的安全连接的步骤。)

这是一个非常简单的黑客，但它将[rgrokett]系统的电池寿命从几天增加到一个多月(他仍在等待，看看它们能持续多久)，所需要的只是微控制器、传感器和几个部件。我们有几个关于让 ESP 模块进入深度睡眠的老黑客，例如[这个](https://hackaday.com/2015/02/08/hack-allows-esp-01-to-go-to-deep-sleep/)一个，并查看这个关于 [PIR 传感器](https://hackaday.com/2009/08/21/passive-infrared-pir-sensor-tutorial/)的教程。