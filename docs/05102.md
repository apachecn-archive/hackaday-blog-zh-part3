# 旧温度计有新眼睛

> 原文：<https://hackaday.com/2017/02/24/old-thermometer-gets-new-eyes/>

尽管我们总是希望有合适的工具来做合适的工作，但有时我们的零件抽屉里会有其他东西。毕竟，有什么比买一个新工具更好的呢？当[他需要一个带数字输出的温度计](http://kurokesu.com/main/2017/02/20/dumb-thermometer-gets-digital-output/)时，至少【Saulius】肯定是这么想的，但手头只有一个笨笨的但功能丰富的温度计。

幸运的是，[Saulius]有一个网络摄像头和一个旧的温度计，由于温度计有一个 LCD 显示屏，所以让摄像头识别温度计显示屏上的数字相对简单。这也不是什么旧温度计。这是一个四通道温度计，具有良好的分辨率和许多其他有用的功能(明显缺乏通信能力)，所以这不是他可以忽视的东西。

一旦相机安装在手臂上并指向温度计的屏幕，计算机上运行的算法就会检测多边形并将其信息报告到 CSV 文件中。这一过程变得更加简单，因为像这样的 LCD 屏幕是非常可预测的。从那里，数据被导入 LibreOffice，并可以制作各种图表和图形。

虽然这可能不是最优雅的方法，但有时您必须使用当时手头的资源。有时候你需要的工具是[太贵](https://hackaday.com/2013/02/08/building-a-tool-to-measure-melting-point/)、[政治危险](http://hackaday.com/2016/05/27/retrotechtacular-examining-music-in-1950s-russia/)，或者[太不切实际而无法获得](http://hackaday.com/2014/12/20/first-ever-parts-emailed-to-space/)。为此，[Saulius]的黑客是一个很好的例子，说明在正确的心态下，什么样的黑客是可能的。