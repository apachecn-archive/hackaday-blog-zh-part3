# 蚀刻 SDR

> 原文：<https://hackaday.com/2015/10/04/etch-a-sdr/>

如果你把软件定义无线电(SDR)和一个标志性的儿童绘画玩具(我们确信这是一个注册商标名称)放在一起，你会得到什么？如果你是[devnulling]，你会得到 Etch-A-SDR。这个盒子使用了 Odroid C1、Teensy 和无处不在的 RTL-SDR。

旋钮作为控制旋钮工作良好(正如你在下面的视频中看到的)。当你听收音机无聊的时候，你可以重置盒子，进入蚀刻-a…嗯，绘图模式。旋钮的工作就像你预期的那样，你甚至可以通过剧烈的晃动来擦除屏幕。

查看项目的存储库，看起来无线电软件是 gqrx，有一些 Python 的修改。剩下的代码混合了 Python、JavaScript、一些 shell 脚本和 Arduino 风格的 C++ ( [向【Elliot】](http://hackaday.com/2015/07/28/embed-with-elliot-there-is-no-arduino-language/)道歉)。

我们已经覆盖了很多 [RTL-SDR 和 SDR 项目](http://hackaday.com/2012/06/27/getting-started-with-software-defined-radio/)，包括 [Mac 端口](http://hackaday.com/2012/10/08/os-x-port-of-gqrx-is-the-easiest-way-to-get-into-software-defined-radio/)、[传感器黑客](http://hackaday.com/2014/03/31/sniffing-ph-sensor-rf-signals-for-feedback-re-your-esophagus/)和[频谱分析仪](http://hackaday.com/2014/11/19/rtl-sdr-as-a-spectrum-analyzer/)。不过，Etch-A-SDR 无论出现在哪里，都肯定会成为一个话题。当然，我们也谈到了义务相关的[时钟项目](http://hackaday.com/2014/03/28/an-etch-a-sketch-to-fetch-the-time/)。

 [https://www.youtube.com/embed/1YYz0kW67oU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/1YYz0kW67oU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

