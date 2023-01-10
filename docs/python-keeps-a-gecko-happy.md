# Python 让壁虎开心:带树莓 Pi 的玻璃容器自动化

> 原文：<https://hackaday.com/2017/11/21/python-keeps-a-gecko-happy/>

不管是好是坏，宠物经常成为硬件黑客的灵感和测试对象:让仓鼠轮子变得更聪明，从狗的角度发布松鼠狩猎冒险，或者自动和远程控制爬行动物围栏。来自荷兰的壁虎饲养员【TheYOSH】选择了后者，并为树莓派编写了 [TerrariumPi，通过一个方便的网络界面来控制和监控他的异国伴侣的家。](https://github.com/theyosh/TerrariumPI)

正确的生态系统对任何动物的健康和幸福都至关重要，这些动物并非生于不由自主选择的环境。因此，模拟自然栖息地的温度、湿度和光照应该是任何宠物主人的头等大事。模拟过程自动化程度越高，人们就越不需要担心。

TerrariumPi 支持所有常见的温度/湿度传感器和继电器板，可以根据固定的时间间隔或传感器反馈利用加热和冷却、浇水和喷洒以及照明。它甚至支持基于位置的日出和日落模拟——你的小动物可能会认为它从未离开过马达加斯加、新喀里多尼亚或巴西。所有的配置和监控都在浏览器中进行，如[【the yosh】的具有公共读取权限的实时系统](https://terrarium.theyosh.nl/)(荷兰语)所示。

Python 是爬行动物相关系统的语言选择，这似乎很自然。另一方面，它不一定要严格用于爬行动物甚至是水族箱；TerrariumPi 将同样出色地照顾好水族馆和任何其他类型的动物馆。毕竟，我们以前见过树莓码头[处理温室](https://hackaday.com/2017/08/26/raspberry-pi-is-the-brains-behind-automated-greenhouse/)和[自动化蘑菇栽培](https://hackaday.com/2015/02/08/automated-mushroom-cultivation/)。