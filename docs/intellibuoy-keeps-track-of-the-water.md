# 智能浮标跟踪水

> 原文：<https://hackaday.com/2017/11/29/intellibuoy-keeps-track-of-the-water/>

随着世界海洋的清洁程度从非常肮脏到天啊，我们需要弄清楚到底发生了什么。新泽西州哈肯萨克的高中生建造了智能浮标，一种漂浮的水质传感器。浮标顶部有一个风速计和数字雨量计，以及一个符合海事法规的 LED 信标。

漂浮由密封的 3/4”和 3”PVC 管框架提供，这些管看起来足够坚固，可以保护电子设备免受偶然的船只撞击。在水面上方很高的地方(在理想条件下)有一个防水控制盒，里面装有两个 Arduino UNOs，可以监听传感器。浊度传感器测量水中有多少泥沙；其他传感器测量 Ph 值、溶解氧和温度。传感器盒悬挂在一个 PVC 双环内，以提供最大程度的保护。每个 Duino 还配有一个 SD 卡保护罩，用于存储各个传感器的数据。

在不对团队进行过多抨击的情况下，我们认为他们通过插入式笔记本电脑从串行监视器中剪切并粘贴传感器数据来检索传感器数据的想法可能不是最佳解决方案。简单的数据检索非常重要，如果项目要大规模实施，他们需要一个非技术人员也能实施的解决方案——也许是一个“磁盘驱动器”?

我们喜欢密封的 PVC 如何成为保护电子产品防潮的首选方法，以及简单的漂浮方法——我们之前发布的这个[潜水 ROV](https://hackaday.com/2017/02/10/pvc-submersible-rov/) 就是一个很好的例子。

 [https://www.youtube.com/embed/ksbBQ_LR1fg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ksbBQ_LR1fg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

