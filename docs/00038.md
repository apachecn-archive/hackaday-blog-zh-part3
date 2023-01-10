# 更新 Arduino TinyGPS 以支持 GLONASS

> 原文：<https://hackaday.com/2015/09/08/arduino-tinygps-updated-to-support-glonass/>

如今，全球定位系统是一项全球性技术，俄罗斯的 GLONASS 系统和即将到来的欧洲伽利略系统在我们头顶上与最初的美国全球定位系统卫星一起运行。[Florin Duroiu]决定拥抱全球化，通过为 Arduino 平台派生 TinyGPS 库来增加对这些卫星星座的支持。

除了对 GLONASS 的支持之外，备受尊敬的 TinyGPS 的新版本通过加入 [NMEA 3.0 标准](http://geostar-navigation.com/file/geos3/geos_nmea_protocol_v3_0_eng.pdf)增加了一些简洁的新功能(警告:大屁股 PDF 链接)。使用这个，你可以提取有趣的东西，如从每个卫星星座计算的位置，每个卫星的信号强度，以及更多关于卫星对你的 GPS 接收器说什么的技术资料。[Florin]声称它是 TinyGPS 的替代产品，不需要重写。目前还没有对[伽利略](http://www.esa.int/Our_Activities/Navigation/The_future_-_Galileo/What_is_Galileo)的支持(因为卫星仍在发射中:现在有八颗在轨道上)，但【弗罗林】正在寻求帮助来添加这一点，以及一旦投入运行的新的中国[北斗](https://en.wikipedia.org/wiki/BeiDou_Navigation_Satellite_System)系统。

(上图:艺术家对轨道上伽利略卫星的看法，由欧空局提供)