# 一种联网的狗处理机

> 原文：<https://hackaday.com/2017/05/07/the-internet-connected-dog-treat-machine/>

[Eric]和[Shirin]有一只叫[Pickles]的狗，它是那种如果你是一个爱狗人士就会暗暗垂涎的动物。他们显然很喜欢[泡菜]，但面临的问题是他们不能总是在家表达对他的感激。但是他们没有完全抛弃他，而是将技术应用到这个问题上。[Eric]建造了一个联网的狗零食分发器，通过它他们可以分发零食，看着幸运的小狗狼吞虎咽地吃。

机器的主体由激光切割丙烯酸树脂制成，分配器机构是由步进电机驱动的旋转料斗。整个事情——在其所有透明的荣耀中——是通过一个树莓 Pi 控制的，它会播放一段[Shirin]叫[Pickles]请客的声音剪辑，用它的摄像头记录他的用餐享受，并将结果通过电子邮件发送给他的主人。在幕后，它托管着一个 MQTT 服务器，可以通过 iPhone 应用程序、Alexa 或 adafruit.io 网站触发。想象一下:“Alexa，喂我的狗！”。它有一个戒指。

他指出，这台机器不仅仅局限于分发零食，它还可以用于从事更多的活动。他暗示了一个未来的项目，包括一个投球装置(你曾经从一只狗身上看到过这样的快乐吗)。没有什么可以代替和你的狗在一起，但是也许有了这个设备，他们可以让他们的狗的生活少一点，嗯，一只狗的生活。

你可以在我们发布在广告下方的视频中看到这台机器在运转。

 [https://www.youtube.com/embed/Wz0v1ltECgQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Wz0v1ltECgQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



我们过去在 Hackaday 给你带了几个狗零食贩卖机。其中一个使用了[一个倾斜料斗](http://hackaday.com/2013/02/05/web-connected-treat-dispenser-appeases-the-pets/)，一个使用了[一个 CD 轴](http://hackaday.com/2008/12/05/iphone-controlled-dog-treat-dispenser/)，还有[另一个是 3D 打印的](http://hackaday.com/2013/07/10/3d-printed-dispenser-flings-treats-at-your-pets/)。

[via [树莓派 Pod](http://www.recantha.co.uk/blog/?p=16796)