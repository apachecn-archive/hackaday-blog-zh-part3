# 椅子跳舞就像没有人看一样

> 原文：<https://hackaday.com/2016/09/17/chair-dances-like-no-one-is-watching/>

虽然说这张椅子跳舞*可能更准确，因为*没人看，但结果仍然是挪威国家装饰艺术与设计博物馆的常驻设计师【Igor】最近创造的一个聪明的项目。模糊了艺术、黑客和《超级马里奥》(Super Mario)中的幽灵之间的界限[。这张椅子使用一系列令人印象深刻的功能来“跳舞”](http://hyperglitch.com/articles/dancing-laminette)，但前提是没有人看它。

为了让椅子看起来像在跳舞，[Igor]在四条腿上安装了伺服电机，让它们可以弯曲。一个不动的小销钉被放在椅子腿的内侧，以防止椅子在整个过程中倒下。它足够小，从远处看不会立即被注意到，这有助于保持一个跳舞椅子的错觉。

从那里，一个树莓 Pi 3 充当椅子的控制中心。它用 Python 编程，运行 OpenCV 进行面部检测，并使用 [pigpio](http://abyz.co.uk/rpi/pigpio/) 控制腿部伺服系统。还有一个网络界面，用于观看相机的输出和查看其面部识别能力。web 界面还允许用户调试程序。[Igor]的椅子在 800×600 像素的情况下每秒可以处理 3 帧。

请务必在休息后观看视频，了解椅子的运行情况。这是一件有趣的艺术品，如果这些榫钉可以支撑一个人的重量，它将是任何家庭的一个很好的补充。不过，如果椅子不够你坐的话，还有其他更危险的选择。

 [https://www.youtube.com/embed/6EufzsvxsoQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/6EufzsvxsoQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

