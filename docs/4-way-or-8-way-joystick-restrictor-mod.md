# 4 路或 8 路操纵杆限制器模块

> 原文：<https://hackaday.com/2017/01/23/4-way-or-8-way-joystick-restrictor-mod/>

如果游戏手柄内置在只能玩一种游戏的游戏柜中，那么在街机游戏中使用受限的 4 路或 8 路数字游戏手柄是没问题的——4 路用于 Pacman，8 路用于 Super Cobra。但是[Tinker_On_Steroids]想要一个操纵杆，它可以被限制为 4 向或 8 向,用于可以玩许多游戏的柜子，并且它必须根据所选的游戏自动从一种类型的限制切换到另一种类型。

他的[数字操纵杆](https://de.aliexpress.com/item/Free-shipping-2PCS-lot-Colorful-LED-Glitter-Lighted-Illuminated-Joystick-Arcade-Stick-Beautiful-7-color-flashing/32756082816.html)已经配备了一个可以安装 4 向或 8 向限制的板，但它必须手动拧紧到位。他移除了它，并设计了两个 3D 打印部件，一个牢固地安装在操纵杆的底部，另一个在第一个部件内旋转。在一个方向旋转会产生 4 向限制，在另一个方向旋转会产生 8 向限制。剩下的只是附加一个伺服做旋转。下面的第一个视频显示了安装这一切的操纵杆和演示伺服使用 Teensy。零件的 STL 文件在他的 [Thingiverse 项目页面](https://www.thingiverse.com/thing:1984680/#files)上。

他还展示了一个他制作的简单电路板，上面有两个按钮和两个发光二极管，用于连接青少年和控制伺服系统。作为一个附加选项，他展示了如何通过 USB 从他的台式电脑与青少年交谈，并以这种方式控制伺服系统。在下面的第二个视频中，他详细介绍了这一切，并演示了他为 Teensy 编写的代码。在 Thingiverse 页面上，他只提供了十六进制文件，但不管怎样，你可能会编写自己的游戏界面软件。

[Tinker_On_Steroids]并不是唯一一个不得不修改操纵杆以在旧游戏上获得良好游戏性的人。克里斯·奥斯本(Chris Osborn)不得不为他的苹果 II(Apple II)设计一个现代的 USB 游戏手柄，以解决他的旧苹果游戏手柄的问题。或者也许你的[操纵杆磨损了，需要修理](http://hackaday.com/2015/03/27/inexpensively-replace-a-worn-out-n64-joystick/)，就像【狂热融洽】为他的任天堂 64 所做的那样。

 [https://www.youtube.com/embed/pQ01ksbe_Bg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/pQ01ksbe_Bg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/C653B6JIBXI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/C653B6JIBXI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[EVR]的提示。