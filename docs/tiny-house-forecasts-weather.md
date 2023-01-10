# 小房子预报天气

> 原文：<https://hackaday.com/2016/09/15/tiny-house-forecasts-weather/>

在信息时代之前，收集天气信息并不容易。当然，有温度计、气压计和关于天空的韵律，但如果你当时住在德国或附近，你可能也有机会接触到一种叫做“天气房子”的东西，它可以帮助预测降雨。[Moritz]又名[Thinksilicon]发现了一个类似的设备，并着手对其进行现代化改造。([谷歌翻译自德语](https://translate.google.com/translate?sl=auto&tl=en&js=y&prev=_t&hl=de&ie=UTF-8&u=http%3A%2F%2Fthinksilicon.de%2F78%2FWetterhaeuschen-mit-WLAN.html&edit-text=&act=url))

传统的气象房本质上是一个装在复杂艺术品中的湿度计。两个人物，通常是一男一女，被一小段马鬃悬挂在中间的平台上保持平衡。当湿度较低时，头发会收紧并向一个方向转动平台，当湿度较高时——表明要下雨了——它会向另一个方向转动。当男人从房子里出来时，它就预示着降雨。

为了升级天气预报室，[Moritz]在前面安装了一个有机发光二极管显示器，取代了传统的温度计。他没有用马毛来旋转数字，而是在平台上安装了一个小型伺服系统。整个房子由一个 ESP8266 控制，它从[开放天气 API](http://openweathermap.org) 中提取数据，并根据接收到的信息旋转数据。

就像独特的时钟一样，我们喜欢有趣的天气指示/预报。这就好比[用松鼠预测天气](http://hackaday.com/2016/07/28/squirrel-cafe-to-predict-the-weather-from-customer-data/)，或者在你的书架上放一个小型的[天气娱乐](http://hackaday.com/2012/11/15/an-extemely-unique-weather-display/)。