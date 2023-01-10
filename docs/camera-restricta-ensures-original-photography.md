# 相机限制确保原创摄影

> 原文：<https://hackaday.com/2017/01/28/camera-restricta-ensures-original-photography/>

适当的记录很重要，旅行时通常通过摄影来实现。多余的文件往往是低效的，而[相机限制](http://philippschmitt.com/projects/camera-restricta)——在一篇关于摄影地标饱和度的评论和最近一场关于欧盟摄影审查的辩论中——旨在挑战摄影师拍摄独特的照片。

相机 Restricta 有一个 3D 打印的机身，内置一部智能手机，用于 gps 数据、显示和音频输出，而 ATTiny85 则用于控制相机的阻断功能。当用户设置使用 Camera Restricta 拍照时，手机上运行的一个应用程序会查询 node.js 服务器，该服务器会在 Flikr 和 Panoramio 上搜索本地的地理标记照片。根据这些信息，相机会输出与拍摄照片数量相关的咔哒声，如果该地区的照片数量超过一定数量，屏幕会触动连接到 ATTiny 85 板上的光电池，收回快门按钮并锁定取景器，直到找到更具原创性的拍摄对象。

[https://player.vimeo.com/video/137595414](https://player.vimeo.com/video/137595414)

让一个人的相机对着我们关闭听起来令人恼火——特别是当音频输出听起来几乎像是世俗的盖革计数器时——但由此产生的寻找原始主题的冒险可能值得努力。

为了确保这些原始照片在你自己上传之前保持原样，一点点的秘密摄影可能是合适的。

【谢谢提示，意泰！]