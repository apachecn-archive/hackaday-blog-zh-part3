# 感觉帽子活了

> 原文：<https://hackaday.com/2017/05/27/sense-hat-comes-alive/>

还记得覆盆子 Pi Sense 帽子吗？最初是为国际空间站的任务设计的，板上有相当多的传感器以及 8×8 RGB LED 矩阵。你能用 8×8 的屏幕做什么？如果你用【伊森的】 [Python Sense Hat 动画库](https://github.com/EthanTamasar/python-sense-hat-animation)你可能会很惊讶。你可以在下面的视频中获得完整的视觉效果。

代码使用一个数组来表示屏幕，这没什么大不了的，因为只有 64 个元素。无论有没有这个库，打开一个特定的元素来制作动画，比如说一个乒乓球，并不困难。下面是使用该库完成此操作的一些代码:

```
for x in range(0,7):
 ect.cell(image,[0,x],[randint(0,255), randint(0,255), randint(0,255)],0.1)
 ect.cell(image,[0,x],e,0.1)
for x in range(7,0, -1):
 ect.cell(image,[0,x],[randint(0,255), randint(0,255), randint(0,255)],0.1)
 ect.cell(image,[0,x],e,0.1)
```

每个循环用随机颜色画一个方框，然后在转到下一个位置之前擦除它。第二个 for 循环使圆盘向相反方向移动。您大概可以推断出第一个参数是屏幕数组，第二个是位置。第三个参数设置颜色，最后一个参数设置动画计时器。但是，看看代码，它看起来确实像计时器块，这可能对某些应用程序不起作用。

如果只有这些，这不会值太多钱，但是你也可以画三角形、圆形和正方形。例如:

```
ect.circle(image,(4,4), 3, [randint(0,255), randint(0,255), randint(0,255)], 0.1)
```

我们不久前讨论了感觉帽子。当然，正如你从这个[天气仪表盘](https://hackaday.com/2015/10/25/raspberry-pi-sense-hat-super-weather-dashboard/)看到的，它不仅仅是点亮 led。

 [https://www.youtube.com/embed/zX4PD44s-BQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/zX4PD44s-BQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

