# 令人印象深刻的星际争霸 2 AI 对肉肉的对手更公平

> 原文：<https://hackaday.com/2016/03/31/impressive-starcraft-2-ai-more-fair-to-fleshy-opponents/>

Alpha Go 结果发布的时候评论里有讨论。一些评论者假设人工智能研究人员不考虑更具流动性的游戏[，如 RTS 星际争霸](http://graphics.stanford.edu/~mdfisher/GameAIs.html)。

这些评论随后演变成一场讨论，讨论如何让人工智能公平地考虑与人类玩家对抗。很多时候，RTS 游戏中的 AI 之所以赢，是因为他们直接接触到了游戏中的变量。人工智能不是看着屏幕上一个单位所在的小区域，然后移动他们的眼睛来获取战略信息，如准确的位置，生命值，单位等级等，而是立即知道它在 120 倍，2000 年，76%，lvl5 等。人工智能也没有点击延迟，因为它可以直接访问游戏的 API，它只是直接改变一个单位的变量和动作队列。

所以我们对[Matt]的星际争霸 AI 很感兴趣，它要求计算机实际上看着游戏板并点击。[Matt]的人工智能没有看到使用 OpenCV，这以其自己的方式迫使计算机以一种对它来说不自然的方式来看。相反，他编写了一些代码来拦截对 DirectX 库的幕后调用。

然后，计算机能够使用纹理信息和发送到库的其他片段来确定它正在查看什么。不像人工智能直接看到变量，它必须翻译这些变量，并保持自己对地图和情况的印象。例如，如果一个建筑被摧毁，它必须查看地图的那个部分，对照控制测试它所看到的，然后从列表中删除该建筑。

人工智能的一大优势是它的机器人手指。即使这个人工智能必须点击界面，它也不会像我们其他人一样用一个弱关节的肉质小块来做到这一点。这使得人工智能每分钟疯狂动作(APM)在 500 到 2000 之间。

人工智能只在星际争霸的内置作弊机器人上测试过。到目前为止，它可以赢得大多数对硬级别机器人的游戏。如果你想看人工智能正在看的视频，请在休息后查看。

 [https://www.youtube.com/embed/FBZT2ukipkc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/FBZT2ukipkc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

