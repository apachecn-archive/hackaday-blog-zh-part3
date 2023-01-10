# 低成本雨量计寻找洪水

> 原文：<https://hackaday.com/2017/07/31/low-cost-rain-gauge-looks-for-floods/>

我们已经看到了现在无处不在的 ESP 芯片的许多用途，包括许多荒野监测设备。

凭借一些极具吸引力的解决方案和简单的设计，Pluvi.on 脱颖而出。

很多户外项目都涉及到某种普通的耐候围栏，但这个项目有一个定制设计的亚克力盒子。这个雨量计大约 4 英寸宽，使用一个类似跷跷板的水桶来测量降雨量——一个内置在外壳中的漏斗将水送入雨量计，雨量计记录水桶机制每次倾斜的时间，从而记录降雨的强度。一个打包了 ESP8266 WiFi SoC 的 NodeMCU 将数据发送到云端，帮助预测该地区发生洪水的可能性。

[迪奥戈·托雷扎诺]和[佩德罗·戈多伊]开发了 Pluvi.on，作为巴西圣保罗[红牛地下室黑客驻地](http://www.redbullstation.com.br/residencia-hacker-conheca-o-projeto-pluvi-on/)的一部分。对[打造自己的 Pluvi.on](http://www.instructables.com/id/PluviOn-Pluvi%C3%B4metro-De-Baixo-Custo/) 感兴趣？他们在可指示物上建造台阶。

更多的 ESP 项目在 Hackday 上比比皆是，包括这个 [ESP 迷你机器人](http://hackaday.com/2017/06/16/esp32-mini-robot-packs-sensors-and-4wd/)，一个数据记录[仓鼠轮](http://hackaday.com/2017/05/27/esp32-hamster-wheel-tracker-tweets-workout-stats/)，以及一个 [ESP32 信息显示器](http://hackaday.com/2017/07/03/esp32-display-is-worth-a-thousand-words/)。

[https://player.vimeo.com/video/185031727](https://player.vimeo.com/video/185031727)