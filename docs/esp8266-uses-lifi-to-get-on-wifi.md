# ESP8266 用 LiFi 上 WiFi

> 原文：<https://hackaday.com/2018/06/13/esp8266-uses-lifi-to-get-on-wifi/>

将您闪亮的新 ESP8266 连接到 WiFi 可以简单，也可以复杂。大多数人决定手动添加。有些人找到聪明的方法让这该死的东西自己连接起来。【Eduardo Zola】[利用智能手机屏幕的闪光灯](https://hackaday.io/project/153408-esp8266-screen-set-wifi-credentials)传输他的 WiFi 密码。

通过 LiFi 的力量，一个简单的光敏电阻和一点修修补补就可以让他轻松地向他的 ESP8266 发送凭证——或者任何数据。LiFi 是 Light Fidelity 的缩写，它使用表示数字值的开关状态的光来传输数据。它可以使用可见光，如果需要的话，也可以使用紫外线或红外线。关于这个问题的基本细节，请看我们的 LiFi 入门书。

一个闪烁的液晶显示屏和一个光敏电阻勉强够得上单向 LiFi 系统，但[Eduardo Zola]让它工作了。方法是构建一个电阻分压器，并观察 ESP 上的输入引脚是否有变化。

诀窍是将环境光排除在混合光线之外。这里显示的测试传感器将 LDR 放在一个黑色的帽子里，但[Eduardo]为他的反向手电筒 3D 打印了一个光滑的小外壳，以便与手机屏幕齐平。一次点击和大约半分钟的闪烁屏幕后，Wi-Fi 凭证被转移。这种电路真的可以添加到任何项目中，用于短数据传输。在传感器电路上再多做一点工作，速度可以提高，但限制因素是手机屏幕本身的计时。

由于 ESP8266 有自己的 WiFi 连接，一旦 LiFi 将其接入网络，您可能会使用它进行数据传输。但是任何没有完整用户输入或网络连接的情况都可以从中受益。拿出旧的滚动 LED 矩阵项目，并添加这个作为一种方式来推动新的信息到设备！

 [https://www.youtube.com/embed/jeT3SGQUzRI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/jeT3SGQUzRI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2018](https://hackaday.io/prize) is Sponsored by: [![Microchip](img/20eb9d92b47da4c15177567c02a65727.png)](https://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey)  [![Supplyframe](img/2d012d9fc9c7873688699aeadb4742d2.png)](https://supplyframe.com/)