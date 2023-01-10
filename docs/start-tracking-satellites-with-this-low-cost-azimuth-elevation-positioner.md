# 用这种低成本的方位角-仰角定位器开始跟踪卫星

> 原文：<https://hackaday.com/2017/11/26/start-tracking-satellites-with-this-low-cost-azimuth-elevation-positioner/>

跟踪卫星和国际空间站相当容易。你真正需要的是一个 SDR 加密狗或手持收发器，一个简单的自制天线，以及一个清晰的天空视野。将天线对准经过的卫星，你就可以开始听了，或者，如果你是一个有执照的业余爱好者，那就说吧。但是令人厌烦的是指指点点。站在田野里或高楼顶上挥舞着天线会很累，除非你想锻炼手臂，否则就限制天线的尺寸。这就是这个双轴天线定位器可以派上用场的地方。

虽然没有完全达到它最初的目的——定位 1.2 米的碟形天线——[Manuel]确实设法为轻型天线创造了一个非常强大的方位-仰角定位器。更重要的是，他做得很便宜——只有€150 左右。他的设计似乎朝着正确的方向发展，有一个坚固的铝挤压框架和 NEMA23 步进器。但是 3D 打印的部分却成了阿基利的脚跟。在下面的视频中的 1:40 标记处(德语，带英语字幕)，沉重的碟形天线对轴承施加了太多的扭矩，使轴承座分层。但有了细长的碳纤维八木，定位器就大放异彩。运行运动控制的 Arduino 与 GS232 对话，因此它可以直接从网络上获取跟踪数据，以实时控制天线。

希望[曼努埃尔]能解决他的建造中的一些机械问题。也许他可以看看这个用于气象卫星跟踪的巨大碟形定位器来获得灵感。

 [https://www.youtube.com/embed/IhUJTr5AOW4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/IhUJTr5AOW4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

