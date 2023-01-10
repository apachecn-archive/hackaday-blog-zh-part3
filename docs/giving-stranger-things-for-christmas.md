# 给陌生人送圣诞礼物

> 原文：<https://hackaday.com/2018/01/24/giving-stranger-things-for-christmas/>

[鲁道夫]不知道该给他侄女买什么圣诞礼物。原来她是奇怪事物的超级粉丝，所以答案很明显:给她做一面她能控制的字母墙！

缩小比例以适应文档框架，[rudolph]称他们的礼物为 rudLights，这个版本的一个关键参数是使它能够显示从他们侄女的亚马逊 Fire 平板电脑发送的任何短语，而不是不断显示硬编码的短语。为此，它有一个 HC-05 蓝牙模块，可将命令转发给运行在 5V DC 电源上的 NeoPixel LEDs。

[rudolph]在他们儿子的帮助下画出了字母显示器——直接印在主题装饰壁纸上——并在灯泡上切出孔来安装 led。接下来是切割一些纤维板作为牢固的支撑，以便在框架内安装电子设备，并为新像素钻孔。切割和焊接 led 的所有电线是一个小冒险，但一旦完成，[rudolph]将他们的 rudLight 字母表分成三行，并添加电容器以直接接收电力。

 [https://www.youtube.com/embed/wKBw3i2S6m0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/wKBw3i2S6m0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[rudolph]提供了他们用于这个项目的代码——只要确保更改输出 pin 或任何其他与您的构建相关的修改。他们甚至开发了一个应用程序，让控制转向灯变得更容易。如果蓝牙不是你的东西，那么[rudolph]正在努力建立一个 Arduino Pro 迷你版，但没有消息说什么时候会完成。

我们喜欢 Hackaday 的[好道具](https://hackaday.com/2016/07/30/droolworthy-animatronic-stargate-horus-helmet/)或[启发的复制品](https://hackaday.com/2013/04/24/acrobatic-tricopter-inspired-by-the-oblivion-movie-trailer/)，所以这个镶框字母墙在[好公司](https://hackaday.com/2014/10/29/from-nerf-gun-to-rf-cannon-building-a-movie-prop/)里。