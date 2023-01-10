# Hackaday 奖参赛作品:抓住 IMSI 捕手

> 原文：<https://hackaday.com/2016/09/23/hackaday-prize-entry-catch-the-imsi-catchers/>

IMSI 捕手是一种非法的移动电话基站，旨在通过劝说附近的移动电话连接到它而不是真正的电话公司塔来拦截来自它们的流量。名字中的 IMSI 代表国际移动用户身份，这是所有手机都拥有的唯一全球标识符。IMSI 捕捉器通常被政府机构用来检测和跟踪特定位置的人，因此是一些争议的主题。

当一项监控技术被以有争议的方式使用时，往往会有反作用。IMSI 捕手们创造了这篇文章的主题，一个安卓系统的 [IMSI 捕手探测器应用。目前这是一项正在进行中的工作，代码发布在 GitHub 库](https://hackaday.io/project/3824-android-imsi-catcher-detector)的[中，但这仍然是对这个相当模糊的世界的有趣观察。](https://github.com/CellularPrivacy/Android-IMSI-Catcher-Detector)

你可能会问，这个应用程序希望检测伪基站吗？在第一种情况下，它将对照已知基站的数据库来检查它所连接的基站的身份。然后，它将通过分析基站的流量和信号强度来识别基站的任何异常行为。最后，它将努力发现手机协议执行过程中的异常情况，这些异常情况可能会将假塔与真塔区分开来。

他们已经取得了一些进展，但强调该应用程序目前处于 alpha 阶段，需要做更多的工作。因此，他们邀请 Android 开发者加入这个项目。尽管如此，致力于项目才是 Hackaday 奖的意义所在。

The [HackadayPrize2016](https://hackaday.io/prize) is Sponsored by:[![Atmel](img/2e52aec37df7a9bb2e83735e78e154fe.png)](https://hackaday.io/atmel) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://www.digikey.com/) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/)