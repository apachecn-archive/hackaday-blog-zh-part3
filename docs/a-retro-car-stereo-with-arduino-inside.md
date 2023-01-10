# 内置 Arduino 的复古汽车音响

> 原文：<https://hackaday.com/2017/06/04/a-retro-car-stereo-with-arduino-inside/>

对于一些热衷于老爷车的汽车发烧友来说，只有原创才行得通。[RetroJDM]例如，他有一辆 20 世纪 70 年代中期的 RA28 丰田 Celica，他花了很大力气寻找一个原始的中控台来替换损坏的原装中控台。

上世纪 70 年代的丰田汽车的中控台只有一个问题，它没有标准尺寸汽车收音机的 DIN 切口，这种标准尺寸汽车收音机自生产以来的几十年里已经变得普遍。相反，它有一个老式的丰田专用收音机的开孔，带有音量孔和突出的中央单元两侧的调谐旋钮，中央单元可能包含调谐转盘和磁带插槽，或者可能是 8 声道的盒式磁带。

他的解决方案很有趣，[他把自己的汽车音响](http://www.retrojdm.com/ArduinoCarStereo.asp)放在一个适合丰田车的外壳里。在收音机内部，有一个 Arduino Mega 控制 Si4703 FM 调谐器和 VMusic3 MP3/USB 音乐播放器以及 PT2314 音频处理器的分线板。为了显示，有一套复古的 LED 七段模块，和一个 MSGEQ7 频谱分析仪。结果就是一台带有调频、线路输入和 MP3 播放器的现代收音机，拥有你所期望的所有功能。虽然没有板载放大器，但这个功能是由一个外部单元完成的。

成品单元以非常专业的前面板收尾，你可以在他的演示视频中看到。

 [https://www.youtube.com/embed/XjDEkCFa69Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/XjDEkCFa69Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



我们在 Hackaday 这里从零开始只有很少的车载收音机，但是我们已经有了不止一个[蓝牙升级](http://hackaday.com/2017/02/21/reverse-engineering-enables-slick-bluetooth-solution-for-old-car-stereo/)或[线路输入端口](http://hackaday.com/2014/01/02/un-crapifying-a-car-stereo/)的增加。

谢谢你的报道。