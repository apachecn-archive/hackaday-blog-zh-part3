# 带 Arduino 的 Dash

> 原文：<https://hackaday.com/2017/02/02/dash-with-arduino/>

亚马逊 Dash 是一项方便的服务，当亚马逊发布他们的 AWS 物联网平台时，[ Brian Carbonette ]觉得它将所有硬件黑客排除在修补乐趣之外。为了寻求公正，他为一个 [Arduino Dash 按钮](https://hackaday.io/project/19351-amazon-dash-button-for-arduino)编写了一份指南，目标是硬件黑客和那些仍在适应这个世界的人。

在他的构建中，[Carbonette]使用了 Arduino MKR1000，为构建你的按钮设计了一些不同的配置选项。他还不遗余力地帮助所有人解决 Arduino-Dash API 通信过程，构建了一个 [AmazonDRS Arduino 库](https://github.com/andium/AmazonDRS)，它处理所有“无聊的细节”，因此您可以专注于硬件。第一次使用时，软件端的设置会很繁琐，在这种情况下，[Carbonette]提供了一个详细的手册来设置前面提到的 AmazonDRS 库，一些示例代码，以及它们的分类。他还建议实现其他功能——比如商品在亚马逊上缺货时的通知——将项目联系在一起。

[Carbonette]还提供了一些关于项目各个方面的外部资源，供那些寻求更大深度和扩展思路的人使用。接下来你知道的事情就是[召唤 Ubers](http://hackaday.com/2015/09/09/press-amazon-dash-button-summon-uber/) 并找到你[遗失的手机](http://hackaday.com/2016/08/31/amazon-dash-button-finds-your-phone/)。