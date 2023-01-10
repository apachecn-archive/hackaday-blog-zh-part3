# 制作一个没有巨大盖子的线圈枪

> 原文：<https://hackaday.com/2017/08/16/making-a-coil-gun-without-giant-caps/>

每当我们在网上看到一个线圈炮项目，似乎都涉及到一堆巨大的电容。[miroslavus]用他的枪采取了一种不同的方法——他希望他的项目建造时没有那些怪物帽。

它由四轴飞行器 LiPo 电池供电，2 个 1400 毫安的无人机电池串联起来，触发 21 个 SWG 铜线圈，[miroslavus]在他设计的[定制 3D 打印缠绕装置](https://www.thingiverse.com/thing:2481600)的帮助下创建了这些线圈。钻机有脊，以帮助您整齐地放下线圈，它们也有光电二极管的安装，确保枪知道什么时候加载。

当被触发时，Arduino Nano 激活一对 IRF3205 MOSFETS，逻辑信号升压至 20V，拍摄长度为 7 毫米或 8 毫米的钢棒。这种枪在发射时并没有产生等离子体放电，但它仍然是一个迷人的项目。

查看我们之前发布的[一次性相机线圈枪](http://hackaday.com/2017/01/07/disposable-camera-coil-gun/)项目和[新手线圈枪](http://hackaday.com/2016/08/19/coil-gun-for-newbies-learning-electromagnetic-propulsion/)帖子。

 [https://www.youtube.com/embed/pFFZcaWAxLg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/pFFZcaWAxLg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

