# 如何不造 CPU 暖手器

> 原文：<https://hackaday.com/2016/11/12/how-not-to-build-a-cpu-hand-warmer/>

冬天来了，伴随着手套、冰冷的手、雪和夹克。既然我们都把锂电池放在口袋里，那么做一个电子暖手器不是很好吗？那就是【GreatScott！]思想。为了制造他的电子暖手器，他转向了将电转化为热的最有效和高效的方法:[一个十年前的 AMD CPU](https://www.youtube.com/watch?v=Bw2p-Dmn48U) 。

制造一个电子暖手器非常简单。你只需要一个电阻加热元件(比如电阻器)，一个限制电流的装置(比如电阻器)，一个电源(比如 USB 电源组)。把这些东西连在一起，你就有了一个效率不是百分之零就是百分之百的暖手器。我们还没搞清楚最后一部分。

因为越强大越复古越好，[GreatScott]从一台旧电脑里拉出了一个 AMD Sempron。显然，查找和阅读数据手册是为懦夫准备的，所以[GreatScott]只是用可变电源戳了戳一些引脚，直到 CPU 在 5V 时消耗了大约 500mA。

视频继续进行一些基于 Arduino 的温度测量，找到一些新的引脚来插入电源线，并用热胶固定这个加热元件上的所有电线*。对于评论中准备说“不是黑客”的人，我们向你保证，这是合格的。*

随着天真的方法建立一个 CPU 暖手的方式，这里的利弊，这个项目，以及如何可以做得更好。首先，使用旧的 AMD 处理器是一个好主意。这些东西是引爆器，即使这个处理器早于 100+W TDP AMD CPU，它也应该足够好了。

也就是说，这不是你在 CPU 中浪费能量的方式。理想情况下，处理器应该做一些工作，更多的活动门会导致更高的功耗。如果这是一个非常旧的处理器，一个好的简单的选择是让芯片自由运行，或者让 CPU 通过它的地址空间计数。这可以通过将地址线连接到低电平或高电平来实现，具体取决于芯片。那会浪费大量的能量。随机戳针希望正确的功耗不是让这个 CPU 发挥最大热量的方法。

当然，上面那段只是理论。吃在布丁里，或者其他一些毁容的口语，所以[这里有一个四核 386 咖啡加热器](https://hackaday.io/project/2621-quad-386-coffee-heater)。来自[magnustron]的这个项目使用四个通过 USB 供电的 80386 CPUs 来为你的 cuppa 制作一个漂亮的桌面电炉。当然，由 USB 供电意味着只有 500 毫安，δT 可以与[GreatScott]的 AMD 和热熔胶暖手器相媲美。这样我们就到了问题的关键:5V 和 500mA 不是很热。在廉价的 10 或 12 瓦 USB-C 电源从中国涌入之前，USB 供电加热器的想法是徒劳的。不过，它确实创造了一些很棒的 AMD firestarter 笑话，所以我们必须为此给予[GreatScott]信任。

 [https://www.youtube.com/embed/Bw2p-Dmn48U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Bw2p-Dmn48U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

