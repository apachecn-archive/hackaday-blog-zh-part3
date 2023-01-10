# 使用 FPGA 从视频中生成环境颜色

> 原文：<https://hackaday.com/2016/05/20/using-an-fpga-to-generate-ambient-color-from-video/>

我们都应该熟悉电视环境照明系统，如飞利浦的 Ambilight，这是一种围绕电视外围的 LED 灯环，可以将屏幕边缘的颜色扩展到周围的照明。[Shiva Rajagopal]受到导师的启发，研究从视频帧中生成更准确的颜色表示的机制，[制作了一个使用 FPGA 实时执行任务的项目](https://people.ece.cornell.edu/land/courses/ece5760/FinalProjects/s2016/svr24/svr24/index.html)。这不是一个流光溢彩的克隆，相反，它的目的是产生尽可能准确的颜色表现，给人一种在空荡荡的房子里为了安全起见而开着电视的印象。

担心的是，简单地平均像素颜色值会产生颜色，但不一定会产生人眼感知的相同颜色。他详细介绍了 [RGB](https://en.wikipedia.org/wiki/RGB_color_space) 和 [HSL](https://en.wikipedia.org/wiki/HSL_and_HSV) 色彩空间之间的差异，并得出了一个等式，该等式考虑了每个像素的饱和度以及人眼对它的感知程度，从而对每个像素进行了重要性评级。因此，他可以通过查看这些重要的像素而不是太暗或太饱和的像素来获得最终的整体颜色，用户的眼睛不会注意到这些像素的颜色。

整个项目制作在一个 [Altera DE2-115](http://wl.altera.com/education/univ/materials/boards/de2-115/unv-de2-115-board.html) FPGA 开发与教育板上，并利用其 NTSC 和 VGA 解码示例代码。他的所有代码都可以在他的[附录](https://people.ece.cornell.edu/land/courses/ece5760/FinalProjects/s2016/svr24/svr24/index.html#appendices)中找到，他还制作了一个演示视频，在休息时间下面展示。

 [https://www.youtube.com/embed/jbla_nbcfxk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/jbla_nbcfxk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



这不是我们在 Hackaday 上介绍的这个领域的第一个项目。我们已经有了[另一个 FPGA 项目](http://hackaday.com/2015/04/25/fpga-based-ambilight-clone/)，一个基于树莓 Pi 的[，以及一个对 RGB 输出求和的](http://hackaday.com/2014/05/18/a-raspi-ambilight-with-hdmi-input/)[完全模拟版本](http://hackaday.com/2012/06/27/simple-ambilight-clone-is-just-a-few-transistors/)。这个项目带来了新的变化，不是通过它做了什么，而是通过它解决问题的方法和它对相关过程的清晰解释。

经由【布鲁斯之地】。