# 用 3D 打印机暴力破解密码

> 原文：<https://hackaday.com/2017/12/15/brute-forcing-passwords-with-a-3d-printer/>

我们中的许多人使用 4 位 pin 码来锁定我们的手机。Hak5 的 David Randolph 想出了一个简单的方法，用 3D 打印机暴力破解这些密码。几乎所有的 3D 打印机都说同一种语言，g 代码。同样的语言在 CAD 和 CNC 机器中使用了几十年。

[David]在他的打印机床上放了一个数字键盘。然后他绘制出每个键的高度和位置。一旦他知道了按键的绝对位置，就很容易告诉打印机移动到一个按键，然后按下并释放。他甚至创建了一个 g 代码文件，可以按下 10，000 个 4 键密码组合中的每一个。

不过这么大的文件有点笨拙，所以[David]也创建了一个 python 脚本来做同样的事情——输出 g 代码和坐标来暴力破解任何 4 针键盘。虽然打印机比 Hak5 自己的 [USB 橡皮鸭](https://hackaday.com/2016/10/28/duckhunting-stopping-rubber-ducky-attacks/)设备(充当自动化键盘)慢很多，但它将成功地暴力破解密码。虽然现在大多数手机都限制用户输入密码的次数。

[David]承认这在秘密/黑客应用中可能没有用，但该视频仍然是对 g 代码和使用 3D 打印机进行非打印功能的很好介绍。

 [https://www.youtube.com/embed/IR8k4uYnTfI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/IR8k4uYnTfI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



有兴趣推动 3D 打印机打印塑料以外的东西吗？你可以随时[打印巧克力](https://hackaday.com/2015/09/26/printing-chocolate-with-a-lego-3d-printer/)。