# 世界上最大、最没用的人工智能机器

> 原文：<https://hackaday.com/2016/09/23/worlds-biggest-most-useless-ai-machine/>

当我们被即将到来的人工智能末日的言论淹没时，很高兴看到一个故意无用的人工智能。那个 AI 是 HAL 9000。不，不是电影《2001:太空漫游》中矛盾的哈尔，而是[世界上最大的人工智能无用机器哈尔](http://rafaelmizrahi.blogspot.com/2016/09/worlds-biggest-useless-machine.html#pages/2)，由【拉斐尔】、【米奇】和【埃亚尔】为以色列 [GeekCon 2016](http://www.geekcon.org/) 建造。

高高耸立，闪闪发光的黑色盒子让我们想起了电影中的巨石。但是，在靠近顶端的一个警戒位置上是哈尔的红眼。当我们接近时，电影中哈尔的声音问我们:“戴夫，你到底在做什么？”因为眼睛的直径随着讲话的幅度而变化。底部有一个亮黄色的控制杆，标着 ON，当然我们只需要关掉它。当我们这样做时，它下面的一个面板打开，一个杆向上延伸，将杠杆转回到 ON 位置。

幕后是两个 Arduinos。一个 Arduino 管理面板和杆的伺服系统，以及播放电影中 HAL 的随机剪辑。另一个 Arduino 使用 [Arduino TVout 库](http://playground.arduino.cc/Main/TVout)输出到位于红色扩散器(即眼睛)后面的投影仪。Arduino 还从麦克风接收输入，并根据振幅，让投影仪投影相应直径的白色圆圈，使眼睛的外观发生变化。休息过后，你可以在视频中看到这一切。

 [https://www.youtube.com/embed/WFMVLnMZPZ4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/WFMVLnMZPZ4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



矛盾的是，无用的机器服务于有趣的目的，我们在过去见过其他有趣的机器，比如一个在你点燃蜡烛的那一刻[熄灭蜡烛](http://hackaday.com/2014/06/19/this-useless-machine-now-plays-with-fire/)和另一个[用木眼翻动书页并扫描它们](http://hackaday.com/2016/08/01/the-most-useless-book-scanner/)。所以，在不浪费时间找乐子的同时，去看看吧。