# Hacklab 的标志随着甜菜植物的栖息地而变化

> 原文：<https://hackaday.com/2017/05/12/hacklabs-logo-changes-with-the-habitat-of-a-beet-plant/>

西班牙萨拉戈萨，hacklab La Remolacha(“甜菜”)展示了一个标志，这个标志[回应了人类与空间中生长的甜菜植物的互动](http://www.laremolachahacklab.com/)。传感器可以跟踪空气和地面的温度和湿度，而按钮可以添加更多的水、植物养料、光线和音乐。

可视化的形状和活动对传感器做出响应。温度越高，形状中的褶皱越多。土壤湿度越大，扭曲越严重，而空气湿度越大，旋转速度越快。添加食物增加了可视化的大小，音乐触发了更多的振动。

Arduino 会跟踪按钮和湿度传感器，而附近一台通过 USB 连接的计算机会将数据发送到 node.js 服务器。数据通过在 WebGL 中完成的 torus 可视化显示在网站上。

甜菜的环境也标志着空间的健康，因为如果没有人参观，就没有人可以喂养植物。另一方面，太多的游客真的会毁掉这个东西吗？

这个项目是由[Innovart]、[Miguel Frago](http://www.12caracteres.com/)和[[Santi Grau](http://proper-code.com/)在其他人的帮助下创建的。

感谢[Esther Borao Moros]的提示！

 [https://www.youtube.com/embed/cPsRi0IJ_Lc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/cPsRi0IJ_Lc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

