# 指向并点击物联网按钮

> 原文：<https://hackaday.com/2017/03/08/point-and-click-to-an-iot-button/>

ESP8266 等廉价 WiFi 板的出现意味着你可以廉价地将项目放到网络上。但是仍然存在如何将这些设备可靠地连接到其他地方的问题。一个试图让所有努力都指向并点击的开源项目是[mongose OS](https://mongoose-os.com/)。开源系统可以与 ESP8266、ESP32 和其他几个平台一起工作。它与亚马逊的物联网后端集成得很好，但并不局限于此。

每个人都想成为你的物联网经纪人，我们看到旨在占领该市场的产品定期出现(和消失)。从小型设备向远程服务器发送和接收消息的一种常见方式是 [MQTT](https://hackaday.com/2016/05/09/minimal-mqtt-building-a-broker/) ，这是一种 ISO 标准，是为资源有限的设备而制定的。许多物联网服务都使用这种协议，包括[亚马逊的物联网](https://aws.amazon.com/iot/)产品。在下面的视频中，您可以看到使用 ESP8266 制作亚马逊物联网按钮有多快。虽然视频示例使用 Amazon，但是您可以配置系统与任何公共或私有 MQTT 代理对话。

称 Mongoose 为操作系统可能有点夸张。它确实更接近于我们所认为的“中间件”,但是它确实提供了许多网络和文件系统服务。它还简化了远程部署，并支持对设备进行安全的无线更新。看起来他们也做了很多工作来帮助保护设备。

如果你需要一个真正的操作系统，猫鼬可以和一个真正的 RTOS 坐在一起，比如 FreeRTOS。您可以用 C 或 JavaScript 编码，正如您将在视频中看到的那样，如果您可以利用其中一个内置示例，您甚至不需要太多 C 或 JavaScript。总的来说，它看起来很有成效。

MQTT 非常简单，所以使用它实际上不需要任何支持。然而，Mongoose 带来了很多其他东西，比如安全性和更新，以及可移植性。如果你想比较和对比， [MQTT 无线门铃](https://hackaday.com/2017/03/02/wireless-doorbell-hacked-into-hands-on-mqtt-tutorial/)项目是非常相似的。请记住，如果你想合并两者，Mongoose 操作系统可以很容易地将消息发送到你的本地 Raspberry Pi，就像发送到亚马逊的服务器一样。

 [https://www.youtube.com/embed/nA3tGsSFngc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/nA3tGsSFngc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

