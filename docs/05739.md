# VR 机甲缺失的一环:口袋里的手机

> 原文：<https://hackaday.com/2017/04/26/vr-mechs-missing-link-the-phone-in-your-pocket/>

在制作一款自制机甲战斗游戏的过程中，Florian 意识到，虽然这个概念对人类来说很直观，但在虚拟现实游戏中实现它具有挑战性。简而言之，当身体感知到运动，但感觉不到预期的加速度和动量时，就会发生晕动病。独立于向前运动而变化的驾驶舱视野加剧了这一问题。

为了解决这个问题，[Florian]想用一把转椅来代表转动机甲的“臀部”。这将控制行进方向，并有助于提供重要的物理反馈。当他意识到他的口袋里已经有一个硬件编码器时，他正在考虑为椅子安装一个硬件编码器:他的 iPhone。

通过制作一个访问智能手机方位 API 的 HTML 页面，不需要安装任何应用程序就可以通过 Unity 中的 WebSocket 将手机方位发送到他的游戏中。他实际上旋转他的椅子来驾驶，并使用虚拟现实耳机自由环顾四周，与行驶方向分离。想自己试试吗？从[Florian]的 [GitHub 仓库](https://github.com/fmaurer/Socketphonecontroller)中获取。

下面嵌入了一个视频，但如果你对细节感兴趣，请务必查看[Florian]关于在 VR 机甲驾驶舱中避免晕车的[见解和方法的总结](http://flrnmrr.com/2017/2/28/reducing-vr-locomotion-motion-sickness-mech-cockpit-controls)。

 [https://www.youtube.com/embed/mVOCHHVTcis?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/mVOCHHVTcis?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



这个项目将一个物理元素融入到虚拟现实环境中，但是在另一个方向上也做了很好的工作；给你的固定自行车配上虚拟现实耳机和谷歌街景数据怎么样？