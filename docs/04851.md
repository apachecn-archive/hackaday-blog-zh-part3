# 会说话的 Arduino 告诉 GoPro 该做什么

> 原文：<https://hackaday.com/2017/01/28/talking-arduino-tells-gopro-what-to-do/>

现在是 2017 年，甚至 GoPro 相机现在都有语音激活功能。初露头角的摄像师们，请放心，没有什么比在大型拍摄中反复对着你的相机大喊大叫更专业的了。Hackaday 的校友杰里米·库克(Jeremy Cook)听说了这件事，他没有看到令人讨厌的噱头，而是看到了可能性。[他们可以使用 Arduino 语音命令来自动化他们的 GoPro 吗](https://www.youtube.com/watch?v=d7OaNY3Ofx8)？

毫无疑问，这是实现自动化的一种独创方式。在许多方面，这是有意义的——而不是试图制作自己版本的 GoPro 移动应用程序(冲浪者编写的软件；可怕的 bug)或官方 WiFi 遥控器，坚持你所知道的。[Jeremy]决定将 Arduino Nano 与 ISD1820 语音回放模块配对。然后，这与基于伺服的平移设备相结合——[ Jeremy]希望 GoPro 平移、拍照并重复。Arduino 设置伺服位置，然后命令 ISD1820 在再次旋转之前回放语音命令以拍照。

[Jeremy]报告说，在这个阶段它只是一个原型，并且只能不一致地工作。这可能是录制语音的清晰度问题，也可能是音量问题。很难说语音控制系统会像通过 WiFi 远程控制相机一样强大，但它只是证明了——完成工作的方式从来都不是只有一种。尽管我们已经看到人们更深入地侵入 go pro——看看这个关于如何 pwn 你的 GoPro 的[综合指南。](http://hackaday.com/2014/06/20/pwn-your-gopro-scripting-wifi-and-bus-hacking/)