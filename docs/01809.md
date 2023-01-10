# 呈现垃圾桶的互联网！

> 原文：<https://hackaday.com/2016/03/17/presenting-the-internet-of-trash-cans/>

这迟早会发生。[matthewhallberg]建造了一个[“智能”垃圾桶，它连接到互联网](https://hackaday.io/project/10289-opentrashcan-a-smart-internet-connected-trash-can)，可以由自己的 Android 应用程序控制。我们不确定这个世界是否需要它，但他想要一个，所以建造了它。他以严肃的语气开始，但很快意识到这个构建的有趣部分——休息后看看他有趣的电视购物风格视频。

构建本身并不复杂，可以轻松复制。伺服电机帮助翻盖打开和关闭。这是由超声波 ping 传感器触发的，当有人在垃圾桶前挥手时，它会做出反应。第二个 ping 传感器有助于在容器已满需要清空时通知用户。一个达芬奇带着 Idunio Yun shield 帮助连接垃圾桶和互联网。连接到一组有源计算机扬声器的 mp3 屏蔽增加了垃圾桶的语音功能，允许它播放预先录制的声音剪辑。最后，一个蓝牙模块可以让他将其连接到一部安卓手机上，配套的应用程序可以远程控制垃圾桶。

对于物联网方面的事情，[matthewhallberg]使用 Temboo 帐户在垃圾桶满了的时候向用户发送电子邮件。Arduino 草图，配置 Temboo 帐户的头文件，以及 Android 应用程序都可以从他的博客下载。如果这个项目启发了你，试着建造这个令人敬畏的[机器人垃圾桶，它可以接住你扔在它附近的任何东西](http://hackaday.com/2012/07/20/robot-trash-can-catches-anything-you-throw-near-it/)或[读取被扔出的垃圾的条形码](http://hackaday.com/2013/11/23/oscar-updates-your-grocery-list-from-the-trash/)并更新购物清单。

 [https://www.youtube.com/embed/XlFvMDs3TFM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/XlFvMDs3TFM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

