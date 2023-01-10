# 想要一个低成本的 ARM 平台？抢一个预付费安卓手机！

> 原文：<https://hackaday.com/2015/09/10/want-a-low-cost-arm-platform-grab-a-prepaid-android-phone/>

你愿意花多少钱购买一台 1.2Ghz 双核 ARM 电脑，配有 1GB 内存、4GB 板载闪存、800×600 显示屏和 500 万像素摄像头？我们提到过它也有 WiFi，蓝牙，并且是低功耗设计，包括可以运行几个小时的锂电池吗？15 美元听起来够低了吗？这就是如今你能为一部安卓手机支付的价格。规模经济的无情推进最终给了我们物美价廉的手机。这些是预付费的“一次性”手机，由运营商作为亏本产品出售。成本在蜂窝计划中得到补偿，但这只有在购买者激活所述计划的情况下才会发生。与普通手机不同，激活手机不受合同约束。这意味着你只需花 15-20 美元就能获得所有这些功能，这取决于你在哪里购买。

我引用的规格来自 LG Optimus Exceed 2，目前在美国亚马逊上售价 20 美元。最近几周，同样的套装在零售店也能买到，价格低至 10 美元。Exceed 2 只是现在市场上几款低价 Android 预付费手机中的一款，毫无疑问，这份名单将会改变。如何跟上当前的交易？我们发现了一个不太可能的地方。鼓励农民。Perk 是那种“我们付钱让你看广告”的公司。我们确信有些人确实看了广告，但是大多数人建立了无人机电话的“农场”,通过视频进行传播。无人机为农民赚取积分，这些积分可以转换成现金。这些对我们有什么帮助？为了处理流媒体视频，Perk 农民希望以最低的投资获得最强大的手机。像 [/r/perktv](https://www.reddit.com/r/perktv) 这样的子网站每周都有关于预付费手机的“最佳交易”帖子。也有关于像 Whirl 2 和 Exceed 2 这样的当前流行手机的根源和去模糊的教程。

一旦你有了手机，第一件事就是开机。许多预付费电话试图强迫用户经历激活过程。尽管如此，安装程序总是有一个退出进程的后门。在 Exceed 2 的情况下，只需按下音量增大、音量减小、后退和 home 退出激活过程。

### 有根吗？

有些应用程序需要 root 权限。要做到这一点，你最好的办法是谷歌一下你的手机型号。XDA 开发者论坛是一个很好的资源。虽然预付费手机通常不像旗舰手机那样有社区支持，但你通常可以找到至少一些关于如何扎根于特定设备的信息。迄今为止最著名的“root every device”应用是由 [GeoHot](https://en.wikipedia.org/wiki/George_Hotz) 创建的[tower root](https://towelroot.com/)。你可能还记得第一个越狱 iPhone 的人，乔治·霍兹，又名 GeoHot。他还因 PlayStation 3 的一些安全漏洞而与索尼陷入困境，这也成为了新闻。Towelroot 使用 Linux 内核漏洞(futex)来获取 root 权限。2014 年 6 月发布的 futex 漏洞已在大多数新手机上打了补丁。然而，它还没有在更新相对较少的手机上打补丁，比如预付费手机。在 Exceed 2 上，Towelroot 运行得非常好，甚至不需要重启就可以给用户 root 权限。一旦手机被 root，就需要 SuperSU 这样的 root 权限管理器来跟踪哪些应用程序应该拥有 root 权限。一旦这样做了，一切都会好的！我们发现像 [BusyBox](https://play.google.com/store/apps/details?id=stericson.busybox&hl=en) 这样的包非常有用——尤其是当通过 Android Debug Bridge (ADB)在控制台上工作时。

### 你今天想黑什么？

在这些低价手机和二手手机之间，现在每个家庭似乎都有，有很多设备等待使用。一部备用的安卓手机可以做什么？相当多。学习为 Android 平台编码从来没有比现在更好的时机了。 [Android Studio](http://developer.android.com/develop/index.html) 是目前官方的开发环境。如果你懂一点 Java，就很容易开始制作应用程序。如果你不是 Java 爱好者，但想学习，网上到处都有教程可以帮助你入门。

![tasker](img/8e03e745e3379c5eec4f94080a51d47a.png)不是编码员？自动化 android 设备的瑞士军刀一直是 T2 的任务。Tasker 允许你使用触发器来启动简单的脚本(称为任务),这些触发器可以是任何东西，从插入耳机到连接到特定的 WiFi 接入点，到按下屏幕上的按钮。想要你的智能手机用你自己的主题音乐来通知你到家了吗？只需设置一个 Tasker 配置文件，当它连接到您的家庭 WiFi 路由器时播放一首歌曲。Tasker 本身支持大量的动作，并且可以通过插件进行扩展。Android SL4A 的脚本层)甚至允许它使用 Python 脚本进行扩展。

进入硬件世界，有很多方法可以从 Android 手机上获得 GPIOs。Android [配件开发套件](http://developer.android.com/tools/adk/index.html) (ADK)有点过时了，但它仍然是将 Arduino 板(如 [Arduino Mega ADK](https://www.arduino.cc/en/Main/ArduinoBoardMegaADK?from=Main.ArduinoBoardADK) )与你的设备连接的一个很好的方式。进入硬件领域的另一个选择是 [IOIO OTG 板](https://www.sparkfun.com/products/12633)。顾名思义，这个新版本的 IOIO 板支持 USB OTG 标准。这使得它可以连接手机作为主机或配件。您的项目需要一个简单的无线终端吗？抓住一个终端应用程序和一个串行端口配置文件(SPP)兼容的蓝牙模块，鲍勃是你的叔叔。对使用 ESP8266 进行黑客攻击感兴趣吗？Google Play 商店上有一整页的应用程序[专门用于连接每个人都喜欢的低成本 WiFi 模块。](https://play.google.com/store/search?q=esp8266&c=apps)

我们在这里只是看到了冰山一角。你会用一部备用的 Android 手机，或者这些低成本的预付费设备中的一个来做什么样的黑客行为？请在评论中告诉我们！