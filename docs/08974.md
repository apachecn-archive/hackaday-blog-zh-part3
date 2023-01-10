# 简单的解码器充当索罗哈姆的测试伙伴

> 原文：<https://hackaday.com/2018/03/31/simple-decoder-serves-as-solo-hams-test-buddy/>

对于一个表面上完全是为了接触某人的爱好来说，业余无线电可能经常是一项孤独的活动。许多火腿制造和试验无线电设备比他们实际上在广播中多得多，迭代地改进他们的设备。不过，构建-测试-调整-重复的循环可能会有点乏味，尤其是当你试图评估信号强度和范围，却找不到人给你报告的时候。

为了结束现场测试，【威士忌酒吧】组装了一个简单的业余无线电场确认单元，非常精巧。它依赖于这样一个事实，即几乎所有为野外使用而设计的业余无线电都在麦克风或收发器本身中集成了 DTMF 编码器。几十年来，火腿一直使用按键音作为[带内信令](http://hackaday.com/2017/09/05/in-band-signaling-dual-tone-multifrequency-dialing/)来控制他们的中继器，即使引入了更新的数字控制方法，良好的老式模拟 DTMF 仍然存在。该设备包括一个 DTMF 解码器，连接到一个便宜的手持对讲机的耳机插孔。当接收到 DTMF 音调时，连接到解码器的 NodeMCU 调用 IFTTT 作业，将密钥作为 SMS 消息回送到[WTH]的手机。这样就很容易开车四处转转，测试他的移动钻机是否正在出来。由于接收器非常便携，所以测试的安排有很大的灵活性。

关于业余爱好吃火腿的争论？[我们不怪你](http://hackaday.com/2016/12/12/my-beef-with-ham-radio/)。但是像这样有趣的项目是获得许可并开始实验的完美借口。

 [https://www.youtube.com/embed/awtYq25KpOQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/awtYq25KpOQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

