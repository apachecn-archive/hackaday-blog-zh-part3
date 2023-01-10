# 智能儿童座椅旨在防止悲剧发生

> 原文：<https://hackaday.com/2017/04/21/smart-child-seat-aims-to-prevent-tragedy/>

对我们大多数人来说，记忆缺失就像忘记把垃圾带到路边一样无害，或者可能像开车前把手机和一杯咖啡留在车顶一样昂贵。但是，当婴儿在停车场安静地睡在汽车座椅上时，你会忘记，结果可能是致命的。

毫无疑问，儿童检测系统将很快成为汽车上的标准设备，就像现在的倒车摄像头和后备箱逃生杆一样。不愿意等待，[ayavilevich]提出了他自己的用于儿童座椅的[汽车占用传感器](https://www.instructables.com/id/Fochica-Forgotten-Child-in-Car-Alert/)(更新:我们最初链接到 Instructable，但[ayavilevich]写信来提到[这是实际的 Hackaday 奖参赛作品](https://hackaday.io/project/20902-fochica-forgotten-child-in-car-alert)，他正在寻找更多的人参与到这个项目中来)。

该系统被称为 Fochica，意为“汽车中被遗忘的儿童警报”，目前显然是一个概念证明，但它有潜力。Arduino Uno 通过座椅衬垫下的自制电容传感器和胸部安全带扣中的磁簧开关来感应小家伙在汽车座椅中的存在。智能手机上的安卓应用程序与 BLE 模块配对，以获取传感器的状态，当座位被占用时，手机超出蓝牙范围，应用程序会发出警报。简单，但是有效。

我们喜欢[ayavilevich]考虑得如此周全。像这样的系统最好不要太复杂，所以他所做的任何改进都应该集中在设计一个可靠的、可现场使用的设备上。我们在儿童安全领域展示的另一个技巧是[为视障女孩提供的快速楼梯灯](http://hackaday.com/2016/11/19/stairwell-lights-keep-toddler-with-night-blindness-safe/)，这可能会提供一些想法。

 [https://www.youtube.com/embed/46voDa1xbs0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/46voDa1xbs0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

