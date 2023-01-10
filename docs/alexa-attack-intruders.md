# 阿莱克莎，攻击入侵者

> 原文：<https://hackaday.com/2018/05/08/alexa-attack-intruders/>

如果我们在机器人统治者手中的末日即将来临，我很高兴有机会预览他们将如何应对。这是伊卡洛斯项目背后的想法，这是一个由 Alexa 支持的面部跟踪 Nerf 炮塔。由[Nick Engmann]设计，这个令人印象深刻(或恐怖)的项目是围绕一个 Nerf Vulcan 建造的，这是一个泡沫镖发射机枪，安装在隐藏在下拉式柜门后面的平移炮塔上。这是连接到一个配有 Pi 相机的 Pi 零点。Zero 运行 OpenCV 和谷歌 Firebase，后者将它与亚马逊的 Alexa 服务连接起来。

它是这样工作的:你说“Alexa，打开伊卡洛斯项目”。通过[Nick]创造的 Alexa 技能，它连接到 Pi 并启动系统。如果你说“Alexa，激活 alpha”，它会触发一个继电器打开柜子，Nerf 枪开始四处移动，同时安装在它顶部的摄像头搜索人脸。命令“Alexa，激活 beta”触发 Nerf 开火。

 [https://www.youtube.com/embed/jlsKWUZm6fI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/jlsKWUZm6fI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[Nick]已经完成了一个不错的构建，并编写了过程，因此您可以创建自己的过程。虽然有些有点粗糙:它需要几秒钟的反应时间，所以一个快速的攻击者可能已经在里面了。也许虹膜门和滑出平台会更坚固，增加识别人脸的功能会是一个明智的选择，这样你就不会射错人。