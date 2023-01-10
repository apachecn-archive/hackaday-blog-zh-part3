# DIY 微型单 PCB 合成器

> 原文：<https://hackaday.com/2017/05/09/diy-tiny-single-pcb-synthesizer/>

[Jan Ostman]一直在推动低端 AVR ATMega 微控制器上声音合成的极限，他最近的两个项目非常可爱，我们不得不写下来。 [miniTS](https://janostman.wordpress.com/the-minits-diy-synth/) 与他以前的 TinyTS 共享相同的基本声音生成固件，我们已经在之前[在这里介绍过，但是增加了更多的按键、有机发光二极管和 MIDI，同时去掉了一些旋钮。](http://hackaday.com/2016/12/11/tiny-ts-just-how-small-can-a-playable-synethesiser-get/)

两者都有键盘，只是放置在地平面上的铜垫，代码做简单的电容感应来判断它们是否被触摸。这里的要点是，你可以从[Jan]买到便宜的 PCB，然后用代码做实验。或者你可以拿着代码，用一个廉价的 Arduino 和一些铜板为自己做一个不那么精致的版本。

无论哪种方式，我们都喜欢最少的材料和最大的可调整性的结合，并认为[Jan]分享代码很酷，如果不是 PCB 设计的话。任何有 PCB 布局实践经验的人都可以在一个下午完成一个克隆，尽管批量生产会更便宜，而且你最好从[Jan]那里买一个。