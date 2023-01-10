# 一次一个像素的热全景

> 原文：<https://hackaday.com/2017/05/02/thermal-panorama-one-pixel-at-a-time/>

灵感可能来自最奇怪的地方。从他的“收件箱”中挖掘出一个被遗忘的 Melexis MLX90614 热电堆，【Saulius Lukse】用它建造了一个[全景热感相机](http://kurokesu.com/main/2017/04/18/diy-thermal-vision-shoots-360-panoramas/)。

[Lukse]利用 ATmega328 来控制热传感器，并利用该项目测试他为倾斜和平移设计的一对两个旋转舞台电机，并使用一些滑环来保持它在捕捉场景时的运动。也就是说，一次拍摄一个像素的 720 x 360 全景图像需要一个多小时，并且将所有信息编辑成一张清晰的图片也不是一件容易的事情。偶尔打嗝是图像中的坏像素，但通过平均相邻像素的温度，这些坏像素会很快被填充。

相机设备工作正常——而且确实拍出了很好的照片——但是[Lukse]说，升级后的红外相机可以一次捕捉更大的图像，分辨率也更高，这并不是不受欢迎的。

热电堆的另一个巧妙用途可能会带你走上这个[热手电筒](http://hackaday.com/2013/01/03/an-absurdly-clever-thermal-imaging-camera/)的路线。如果你不[完全建立你自己的](http://hackaday.com/2013/12/01/diy-thermal-imaging-camera/)热感相机。

【谢谢提示，Imn！]