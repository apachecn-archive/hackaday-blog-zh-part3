# 用于医疗培训的 RFID 听诊器喘息和杂音

> 原文：<https://hackaday.com/2017/02/16/rfid-stethoscope-wheezes-and-murmurs-for-medical-training/>

你可能会认为，世界上有多少病人，一个正在接受培训的医生就有多少实践机会。很容易获得治疗感冒和流感等常见疾病的经验，但年轻医生可能需要一段时间才能遇到夹层腹主动脉瘤，而这不是在职培训的时间。

进入 SP，或标准化病人-经过培训向医学生提供信息以模拟特定病例的人。不过，SPs 有一个问题。虽然指导某人讲述反映医疗状况的口述史很容易，但学生最终需要检查 SP，它不会显示与模拟病例相关的任何体征和症状。为了补救这一点，密苏里大学的克里斯·桑德斯和 J·斯科特·克里斯蒂安森开发了一种开源 RFID 听诊器来模拟病人的发现。

这是那种“我怎么没想到呢？”想法。一个便宜的听诊器配有一个 Arduino，RFID 阅读器和一个小音频板。RFID 标签被放置在 SP 胸部和腹部的诊断点上。当听诊器放在一个标签上时，一个特定的声音文件就会从 SD 卡中取出并通过耳塞播放。学生不必问，“我听到了什么？”再也听不到真正的杂音或胎音了。

我们可以很容易地看到这个系统的扩展——RFID 标签触发一台人造超声波机器来显示诊断图像，或者微小的有机发光二极管屏幕将标记的图像显示到耳镜中。开始扩展这个想法的一个好地方可能是[这个数字听诊器记录器和分析器](https://hackaday.com/2012/05/11/digital-stethoscope-can-record-playback-and-analyzer-heart-sounds/)。

 [https://www.youtube.com/embed/dzZYIvY1yrA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/dzZYIvY1yrA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

