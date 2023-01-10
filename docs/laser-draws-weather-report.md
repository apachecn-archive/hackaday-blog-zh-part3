# 激光绘制天气报告

> 原文：<https://hackaday.com/2018/06/23/laser-draws-weather-report/>

你曾经希望激光能告诉你天气吗？如果你有，那么[塔克山农]已经覆盖了你。他发明了一种机器，用激光和一些紫外线敏感纸来画出温度和天气图标。这还不是全部！它连接到互联网上，所以它也可以显示时间和打印信息。

基于[tuckershannon]之前的夜光绘图工作，这台机器内部的大脑是一个树莓 Pi Zero。激光器本身是一个 5mw，405 纳米的激光指示器，按钮是拉链固定的。两个 28BYJ-48 步进电机用于定位激光，一个用于旋转，另一个用于高度角度。每个步进电机都连接到电机驱动板，然后直接连接到 Pi。

支撑激光器的底座和臂是在 SolidWorks 中设计的，然后进行 3d 打印。步进电机相互垂直安装，然后激光指示器安装在末端。电池已经从激光器上取下，终端也直接连接到 raspberry pi。Pi 然后通过 IFTTT 连接到 Alexa，这样就可以在任何地方通过语音控制它。

[tucker]的激光绘图机的真正魅力在于，它可以绘制出温度和天气图标，还可以以数字或模拟形式绘制时间！我们以前看过[塔克山农]的作品。这个项目的前身是他的[时钟，它使用一个带有紫外线 LED 的机械臂来绘制时间](https://hackaday.com/2018/03/22/arduino-clock-jots-down-the-time-in-uv/)和另一个[时钟，它使用类似的机械臂，只带有一个激光](https://hackaday.com/2017/08/29/spell-out-the-time-with-frickin-laser-beams/)。希望我们能看到[塔克]接下来的进步！

 [https://www.youtube.com/embed/Ll1u_rkKWxM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Ll1u_rkKWxM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

