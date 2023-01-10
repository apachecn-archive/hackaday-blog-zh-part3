# 按下亚马逊破折号按钮，召唤优步

> 原文：<https://hackaday.com/2015/09/09/press-amazon-dash-button-summon-uber/>

现代生活很复杂。当你想叫一辆优步汽车来接你时，你必须打开应用程序，登录并设置你的接车地点。[Geoffrey Tisserand]每天使用优步上下班，所以他想出了一个简洁的方法来自动化这个过程，通过对亚马逊 Dash 按钮重新编程来调用优步。他所要做的就是按下按钮，几分钟后，一辆优步轿车来到了他的门前。

为了做到这一点，他使用了[拦截方法](http://hackaday.com/2015/08/10/hacking-the-amazon-dash-button-to-record-whatever-you-want/)，在另一台计算机上运行的 Python 脚本注意到亚马逊 Dash 按钮加入了他的家庭 WiFi 网络，并向优步发出请求。因为优步使用 OAuth 认证系统，所以他能够使用 [Expressjs](http://expressjs.com/) 轻松登录系统。因为他总是遵循相同的路线，他还可以自动张贴接送位置，因为它们不会改变。这是一个节省他时间的巧妙方法，但它没有解决让你知道汽车需要多长时间到达，或者优步是否处于[高峰价格](https://help.uber.com/h/6c8065cf-5535-4a8b-9940-d292ffdce119)的问题。也许这在版本 2 中行得通:一个带液晶显示屏和警示灯的小按钮。