# 语音识别打字机

> 原文：<https://hackaday.com/2016/02/17/the-voice-recognition-typewriter/>

带有语音识别功能的打字机已经存在了一百多年；他们被称为秘书。机器人现在正在承担所有的工作，最后听写和打字是一项可以由计算机处理的工作。[Zip Zaps]使用了一台旧的 Smith Corona 打字机来自动化将口述内容转换成打印文本的过程。就像《广告狂人》*第一季中，一名秘书俯身在一台不合时宜的 IBM 电动打字机上一样，这个机器人将接受口述，并接受 20 世纪 60 年代曼哈顿广告公司公开的性别歧视。*

 *这台打字机不是几个生物执行器的阴谋诡计，而是由 Pololu Maestro 伺服控制器驱动的一系列伺服系统控制的。有 12 个伺服系统将一个小致动器向下移动到键上，另外 12 个伺服系统将其他伺服系统移动到键盘正确行的上方。托架返回杆由步进电机、线性轨道和巨型塑料杆驱动。

虽然会使用打字机的机器人令人印象深刻，但真正的技巧是让它做听写。[Zip Zaps]使用了 Windows 中的内置语音识别功能，通过串行端口将字符传输到基于 Arduino 的电子设备。

有用吗？是的，令人惊讶的是。有用吗？嗯，打字机自然有一个更干净，更模拟的语气，你不能用数字格式复制一个老史密斯电晕打字机的打字体验。这种构建只是当今数字电子产品的自然延伸，我们期待在我们当地的星巴克看到有人拥有这种令人惊叹的设备。

 [https://www.youtube.com/embed/rNSCL4YOd5E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/rNSCL4YOd5E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

*