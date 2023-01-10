# 具有激光点精度的实时行星跟踪器

> 原文：<https://hackaday.com/2016/12/14/real-time-planet-tracker-with-laser-point-accuracy/>

空间。最后的边疆。不幸的是，在另行通知之前，我们中的绝大多数人都被困在地球上。如果你是专业的业余天文爱好者，你可能已经记住了行星的大致位置。但是，如果你想在舒适的房间里准确地了解它们，同时又能自我教育，那该怎么办呢？[Shubham Paul]已经做了额外的秒差距来建立一个[实时行星追踪器](https://paulplusx.wordpress.com/2016/03/01/rtpts/),使用开普勒定律精确计算它们的位置。

Arduino Mega 提供了大脑，而 3.5 转云台和 180 度倾斜伺服系统则是肌肉。电位计和开关允许行星和模式选择，而 GPS 模块和可选的 MPU9250 陀螺仪/磁力计让它知道你在哪里。最后，一个激光笔在一个封闭的房间里显示出行星的位置。然后是代码:很多代码。

硬件方面的事情——正如[Shubham Paul]所阐明的——看起来有点未完，因为项目的重点是意图指导的软件。他们已经包含了他们为 RTPT 编写的所有代码，为那些希望构建自己的代码的人提供了每个部分的细目分类。

 [https://www.youtube.com/embed/3GE2GkWsGKA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/3GE2GkWsGKA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



有一个额外的步骤来自动对齐北 RTPT，否则你必须手动这样做。但是[舒巴姆·保罗]设计了它，这样即使你移动追踪器，RTPT 也会实时调整它的计算。项目的每一部分都包括丰富的相关信息，而不仅仅是简单的说明，足以让任何潜在的建设者有所准备。

这个黑客完成了任务。如果你追求的是外表，那么在这张依靠视觉暂留的行星地图中，你可以看到创造者技能和天文学的艺术表达。