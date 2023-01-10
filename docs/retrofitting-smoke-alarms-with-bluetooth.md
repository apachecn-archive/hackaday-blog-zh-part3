# 用蓝牙改装烟雾报警器

> 原文：<https://hackaday.com/2016/10/26/retrofitting-smoke-alarms-with-bluetooth/>

每个人的家里都应该有几个烟雾报警器，每个人都应该马上去检查他们的烟雾报警器的电池。也就是说，传统的烟雾报警器也有一些缺点。他们只在你能听到他们的地方工作，这个问题已经被安全公司和物联网解决了一遍又一遍。

与其投资智能烟雾报警器，[Johan] [决定打造自己的物联网烟雾报警器](https://hackaday.io/project/10347-smartalarm)。它非常简单，比你在家装商店里能买到的任何神奇的小玩意都便宜，而且可以重复使用你的旧烟雾报警器。简而言之，这是你需要建立一个互联网连接的烟雾报警器的一切。

烟雾报警器，或者至少是含有少量放射性镅的电离报警器，都是非常简单的装置。在警报器内部，有一个金属罐——一个电离室——带有两块金属板。当烟雾进入这个房间时，几个晶体管就会发出警报。如果你曾经拆开过一个，你也许可以根据记忆重建电路。

因为这些警报器非常简单，所以可以将一些额外的电子设备植入一个五十年来都没有改变的设计中。对于[Johan]的项目，他正在这样做，接入电离室上的一根导线，测量通过蜂鸣器的电流，并添加一个具有蓝牙连接的微控制器。

对于微控制器和无线解决方案，[Johan]已经选定了 TI 的 cc 2650 launch pad。它功耗低，相对便宜，允许空中更新，并具有 12 位 ADC。一旦这个微小的模块完成，它可以相对容易地被锁定为烟雾报警器。任何一部旧手机都可以作为报警网络和互联网之间的桥梁。

将烟雾报警器连接到互联网的想法并不新鲜。安全公司已经这样做了很多年，在 Lowes 或 Home Depot 有很多这样的设备。将 smarts 改装成烟雾报警器的想法对我们来说是新的，而且很有意义:烟雾探测器可靠、便宜、简单。为什么不重用容易的东西，并从那里开始构建呢？