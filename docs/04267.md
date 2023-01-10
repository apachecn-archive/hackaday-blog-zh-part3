# 通过耳机偷听

> 原文：<https://hackaday.com/2016/12/18/eavesdropping-via-headphones/>

我们都知道音箱就是麦克风，麦克风就是音箱，对吧？如果没有，花一点时间把你的耳机插入麦克风插孔，对着它们大喊。这不完全是高保真，但它的工作。

因此，以色列的三名安全研究人员成功地将大多数笔记本电脑上的耳机和麦克风组合输入插孔变成窃听设备就不足为奇了。([在这里以 PDF 格式](https://arxiv.org/pdf/1611.07350v1.pdf)提交，在 YouTube 上有一个强制性的[演示视频，嵌入在下面。)speak(a)r 是一个简洁的概念证明，也是一个可怕的双关语。](https://www.youtube.com/watch?v=ez3o8aIZCDM)

这里几乎没有剥削；只需要求编解码器芯片将其输出转储到输入通道，并监听。音频很弱，但他们充分描述了他们可以从中获得的东西，包括语音或高达 1 Kbps 的带宽。事实上，这种渗透能力在几乎每一个办公环境中都存在，只是等待被使用，这是值得关注的原因。

当然，你可以拔掉耳机，这让我们想到内置硬件的手机。该漏洞假设恶意软件可以访问您的音频设备，因此如果您的笔记本电脑中有麦克风，游戏就已经结束了。请在评论中讨论这个问题。

via [TechCrunch](https://techcrunch.com/2016/11/23/security-researchers-can-turn-headphones-into-microphones/) ，感谢【bthy】的提示！

 [https://www.youtube.com/embed/ez3o8aIZCDM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ez3o8aIZCDM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

