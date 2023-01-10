# 使用这款 Raspberry Pi 帧抓取器进行高质量的胶片传输

> 原文：<https://hackaday.com/2016/12/15/high-quality-film-transfers-with-this-raspberry-pi-frame-grabber/>

在 YouTube、iPhones，甚至是简陋的 VHS 摄像机出现之前，业余电影制作人拍摄了数不清的电影。许多这样的镜头仍有待在阁楼和壁橱的顶层发现，当你发现珍贵的家庭记忆宝藏时，你会很高兴有[这款支持 Raspberry Pi 的逐帧电影数字化仪](http://spectrum.ieee.org/geek-life/hands-on/how-to-convert-old-film-reels-with-a-raspberry-pi)供你使用。

乔·赫尔曼(Joe Herman)拿着一台备用的超 8 毫米放映机和一个树莓派(Raspberry Pi ),认为自己具备了保存祖父老电影的好方法。高质量电影传输的秘密是一帧一帧的捕捉，所以[乔]开始彻底检查放映机。原来的电机被废弃，取而代之的是一个速度控制更好的电机，一个磁铁和簧片开关被添加到驱动轴上，以同步每一帧的曝光，光学系统被反转，Pi 的相机安装在内部，LED 光源安装在外部。为了处理源材料的高动态范围，[Joe]编写了 Python 脚本来在多次曝光下捕捉每一帧，并将图像与 OpenCV 相结合。一切都是后来用 FFmpeg 拼接在一起的，如果下面的视频有所提示的话，结果是相当惊人的。

几年前，我们看到了类似的逐帧抓取器构建，但[Joe]的设置很好地集成到了旧投影仪中，看起来真的很好——50 万帧的家族历史和计数。

[https://player.vimeo.com/video/192709862](https://player.vimeo.com/video/192709862)

[via[Geek.com](https://www.geek.com/tech/the-raspberry-pi-is-great-at-digitizing-your-old-timey-videos-1682246/)