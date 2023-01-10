# [乔·格兰德]牙刷播放不烂的音乐

> 原文：<https://hackaday.com/2017/03/27/joe-grands-toothbrush-plays-music-that-doesnt-suck/>

乔·格兰德有一把能在你脑袋里播放音乐的牙刷，这并不令人兴奋。那实际上是制造商耍的一个花招。而是[Joe] [给了他的牙刷一个不吸的音乐的 SD 卡槽](http://www.grandideastudio.com/tooth-tunes-hack/)。

这个项目的~~受害者~~捐赠的硬件是一把名为[牙套](https://en.wikipedia.org/wiki/Tooth_Tunes)的儿童牙刷。它们已经存在很多年了，但是除非你是一个孩子(或者是一个孩子的父母)，否则你不会听说过它们。这是因为他们通常播放汉娜·蒙塔娜和乔纳斯兄弟的悦耳声音，这使得成年人选择蛀牙而不是牙齿健康。然而，如果我们边听安培小时、嵌入式调频或火花隙，我们会倾向于刷掉牙齿的珐琅质。是的，我们正在倡导一种骨导、播客牙刷。

[Joe 的]黑客首先打开刷子的颈部，切断通向刷子后面的传感器的电线(他的第一次尝试很难看，但最后的过程很干净，也很简单)。这使得他可以从手柄中的密封电池盒中取出内脏。在真正的[盛大]时尚中，他推出了一个适合原始尺寸的替换 PCB，添加了一个 SD 卡，并用 ATtiny85 替换了原始的微控制器。他还设计了一个开/关控制器( [MAX16054](https://www.maximintegrated.com/en/products/power/supervisors-voltage-monitors-sequencers/MAX16054.html) )来传递微小的待机电流，以防止电池在医药箱中耗尽，从而使这一技术更加完善。

看看他的视频展示了下面的黑客。你听不到音频演示，因为你必须把这个东西压在头骨上才能听到。原始设备制造商的意思是让它压在你的牙齿上，但现在我们想用它来玩我们自己的黑客。通过骨传导的棒球帽耳机？也许吧。

**更新:**【乔】来信告诉我们他发表了[的音频演示](https://www.youtube.com/watch?v=QIson1FLN_w)。它用一个金属盒作为发声室来代替我们头部的骨头。

 [https://www.youtube.com/embed/nNbroMs_dOQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/nNbroMs_dOQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

