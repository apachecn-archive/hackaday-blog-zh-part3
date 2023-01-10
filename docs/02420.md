# 电脑在板球比赛中击败电脑

> 原文：<https://hackaday.com/2016/05/23/computers-beating-computers-at-cricket/>

一些人认为游戏是让人工智能工作的方式，通过教会计算机如何玩游戏并获胜。这也许是迎接我们新的游戏霸主的第一步:一群康奈尔大学的学生用 FPGA 赢得了一场电脑板球比赛。具体来说，他们想出了如何使用 FPGA 以简洁的方式击败游戏中棘手的击球部分。他们使用 FPGA 直接对游戏电脑的 VGA 输出信号进行采样，检测指示最佳击球时间的仪表图像。一旦它检测到按下按钮的最佳点，它就会触发一个被黑客攻击的键盘来按下按钮，将球打到边界上，得到一个 6 *分。

 [https://www.youtube.com/embed/TcaY5SJkQ9Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent&listType=playlist&list=PL2E0D05BEC0140F13](https://www.youtube.com/embed/TcaY5SJkQ9Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent&listType=playlist&list=PL2E0D05BEC0140F13)



然而，这不仅仅是简单地检测一个发光的像素。学生们必须分析游戏的玩法，并找出如何利用某些怪癖，例如通过检测他们在屏幕上的白色服装来检测击球手是左撇子还是右撇子，然后改变时间以适应。他们还必须从雷达指示器上检测球的速度。所有这些都是在游戏运行的时候。

这是 FPGA 如何有用的一个令人印象深刻的例子:通过巧妙地分析游戏，学生们找到了如何将其分解并创建一个 FPGA 程序，该程序可以使用他们的分析来赢得游戏。我们喜欢光隔离键盘黑客。他们聪明的分析、出色的电路设计和巧妙的实现值得称赞。失陪了，我要去亭子里和我们新的板球霸主喝茶了。

对于那些不熟悉板球的人来说，它就像棒球，但速度只有棒球的十分之一，类固醇更少，茶更多。