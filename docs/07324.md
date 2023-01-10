# 犬速指示器

> 原文：<https://hackaday.com/2017/10/07/dog-pov-canine-speed-indicator/>

[Johan Beyers]构建了一个优雅简单的[狗速度计](https://hackaday.io/project/27596-dog-speedometer)项目，该项目使用 POV 显示器来显示跑步狗的速度，而无需加速度计。使用一个 Arduino(看起来可能是一个 [D-love](https://www.arduino.cc/en/Main/ArduinoBoardDuemilanove) )和一行 5 个 led，[Johan]建立了一个非常简单的 POV — [39 行代码](https://github.com/jbeyers/speevo)——它可以暂停闪烁，以便固定的观众可以看到狗的速度。你怎么知道你的小狗的奔跑速度？这就是这个项目的美妙之处。

不是把所有的发光二极管排成一行，而是排成 V 字形。由于这种空间偏移，图案以正确的速度闪现[。每个数字以不同的速度闪烁，所以你只需寻找失真最小的数字。](http://johan.beyers.co.za/2017/10/06/building_a_speedometer_for_my_dog.html)

[Johan]的代码只做完成工作所需的事情。字符数据存储在数组中，直接回放到 PORTD 的引脚上——避免了大多数常见的 Arduino 风格的复杂的引脚定义和其他愚蠢的事情。

POV 显示器可以用来为任何项目增添活力——我想到了这个[光盘 POV 时钟](https://hackaday.com/2013/09/28/cd-rom-pov-clock/)和这个[风力 POV 气象站](https://hackaday.com/2012/03/02/wind-powered-pov-weather-station/)。