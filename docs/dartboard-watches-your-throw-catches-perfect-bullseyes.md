# 飞镖靶观察你的投掷；捕捉完美的靶心

> 原文：<https://hackaday.com/2017/03/22/dartboard-watches-your-throw-catches-perfect-bullseyes/>

有些人真的花了很大力气来操纵这个系统。当你可以花时间建造一个非常复杂的自动靶心镖靶时，为什么要花数年时间练习一项技能并磨练你的技术以在飞镖中击中完美的靶心？

公平地说，[马克·罗伯]三年前开始的工作看起来是一项非常简单的任务。他想建造一个钻机来移动靶的靶心，以满足任何投掷的预测影响。看似简单，但事实证明相当困难，尤其是当你选择使用自己的动作捕捉系统时。

这个系统是围绕 Nvidia Jetson TX1 构建的，从来没有真正形成，不幸的是，这个事实在项目的头两年里一直在燃烧。[马克]最终求助于价格不菲的[维康 Vantage 运动捕捉系统](https://www.vicon.com/products/camera-systems/vantage)，该系统配有六个红外摄像头。系统跟踪非调节镖上的回射器，并将所得 XY 数据输入 MATLAB，以计算镖的抛物线路径。使用六个步进器的 XY 龙门快速移动棋盘，使靶心处于正确的位置，以捕捉飞来的飞镖。

这是一个巨大的工作量和大量的金钱支出，但当地酒吧的小组似乎很喜欢它。不过，我们想知道是否可以简化。也许用基于 IMU 的动作捕捉系统跟踪投掷者的动作并推断撞击点会有效。

 [https://www.youtube.com/embed/MHTizZ_XcUM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/MHTizZ_XcUM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢提示，[BMS light]！