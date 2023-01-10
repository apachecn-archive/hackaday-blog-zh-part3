# 对 Smart ForTwo CAN 总线进行逆向工程

> 原文：<https://hackaday.com/2017/02/28/reverse-engineering-the-smart-fortwo-can-bus/>

CAN 总线已经成为现代汽车事实上的标准。如今，汽车中的所有电子设备都通过总线进行交流，这让它成为了有抱负的黑客的沃土。[丹尼尔·贝拉斯克斯]正在这个领域努力，试图解码他的 Smart ForTwo 的 CAN 总线上的信息。

[Daniel]遇到了一些问题——第一次尝试使用 Beaglebone Black 在阅读信息方面有些成功，但导致汽车和指示灯出现奇怪的活动。这在任何连接到现有系统的黑客攻击中都是正常的——很有可能会破坏正在发生的事情，导致意想不到的后果。

使用 Arduino 和 MCP_CAN 库的进一步工作使[Daniel]获得了更好的结果，但是更好的理解为什么 BeagleBone 会对总线造成干扰。当你在一辆高速行驶的一吨重的金属死亡车上砍人时，安全是非常重要的，所以对你所做的一切进行再三检查是值得的。

到目前为止，[Daniel]已经完成了记录总线信息的部分工作，找到了包括点火和转向信号的寄存器，等等。在评论中分享你的黑客技巧。对于那些对 CAN 总线感兴趣的人来说，[看看【Eric】关于 CAN 黑客的伟大入门](http://hackaday.com/2013/10/21/can-hacking-introductions/)——并让那些[汽车黑客项目流向提示线](http://hackaday.com/submit-a-tip/)！