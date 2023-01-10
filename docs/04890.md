# 你的手臂是理想的控制器

> 原文：<https://hackaday.com/2017/01/31/your-arm-is-the-ideal-controller/>

随着对可穿戴技术和虚拟现实的兴趣和可及性接近历史新高，来自康奈尔大学的三名学生【达里尔·塞、王川和扎卡里·齐默尔曼】——寻求将你的[身体变成完美的控制器](http://people.ece.cornell.edu/land/courses/ece4760/FinalProjects/f2016/dns55_exw2_dns55/dns55_exw2_dns55/dns55_exw2_dns55/index.html)。

至少这是最终目标。他们的原型包括三个 Kionix 三轴加速度计、陀螺仪和磁力计传感器(位于手部、肘部和肩部)，以跟踪手臂的运动。依靠个人电脑来完成大部分繁重的计算工作，一个装在 t 恤盒子里的 PIC32 嘿，这是一个原型！—从三个关节位置接收数据，通过串行接口将数据传输到所述 PC，从而在虚拟环境中呈现可用的 3D 模型。经过短暂的校准后，该设置跟踪手臂的运动，几分钟内读数只有一点点漂移。

 [https://www.youtube.com/embed/V8UBRQ_a8ZE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/V8UBRQ_a8ZE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[Sew，Wang 和 Zimmerman]将他们的项目视为游戏、虚拟现实、健身和医疗行业现有高端系统的一种易于实施的替代方案。我们迫不及待地想将这与跟踪单个手指结合起来。

如果看到这个项目已经让你对快速原型制作这个话题有所了解，看看他的 SuperCon talk 中关于这个话题的[建议。我们还想指出[Bodo Hoenen 的]关于一个使用](https://hackaday.com/2016/12/01/quickly-prototyping-x-ray-backscatter-machines/)[肌电图来检测手臂](https://hackaday.com/2016/12/09/this-diy-wearable-assist-goes-beyond-traditional-therapy/)肌肉运动的系统的演讲。