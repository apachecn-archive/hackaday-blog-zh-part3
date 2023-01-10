# Pi 驱动的数字窥镜

> 原文：<https://hackaday.com/2016/03/11/digital-zoetrope-powered-by-pi/>

zoetrope 是维多利亚时代的一件迷人作品，它通过旋转鼓上的狭缝曝光连续的画面，给人一种移动图像的感觉。然而[Brian Corteil]并不满足于仅仅是 19 世纪的客厅娱乐，他将 12 个有机发光二极管显示器连接到一个树莓皮上，并将它们安装在一个带有旋转编码器的圆形平台上，制成了一个全数字的窥镜。

将 12 个 SPI 器件连接到 PI 一直是一项挑战，因为只提供了两条 CS 线。[Brian]对这个问题有一个相当优雅的解决方案，他将他的显示器用菊花链连接起来，形成一个移位寄存器，在这个寄存器中，每个图像以旋转增量传递到下一个显示器。

他制作的窥镜放在一个激光切割的框架上，框架在一个编码盘上旋转，这个编码盘看起来是由印刷纸制成的。这仍然是一项正在进行的工作，但他计划在 Pi 摄像机上录制视频，以便立即播放他的创作。你可以看看他在 GitHub 上为 zoetrope 编写的[代码。](https://github.com/Corteil/Zoetrope)

这不是我们在 Hackaday 这里报道的第一个 zoetrope，甚至也不是第一个数字版的。我们已经看到了[的几个](http://hackaday.com/2015/03/25/before-film-there-were-zoetropes-now-we-have-3d-printed-zoetropes/)[的 3d 打印](http://hackaday.com/2012/01/11/3d-printed-zoetrope/)的，还有一个[的特色是用 Kinect](http://hackaday.com/2011/03/19/building-a-zoetrope-using-kinect-processing-and-a-laser-cutter/) 捕捉的激光切割图像。但这是一件很好的作品，如果他的相机计划实现的话，还会有更多的作品。

下面是[Brian]在 Raspberry Pi 4 岁生日派对上制作的 zoetrope 的视频。很抱歉，这是一部巡回黑客作家的照相手机，我们希望它能让人们了解这款手机的功能。

 [https://www.youtube.com/embed/CvFHc7fW6Sw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/CvFHc7fW6Sw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

