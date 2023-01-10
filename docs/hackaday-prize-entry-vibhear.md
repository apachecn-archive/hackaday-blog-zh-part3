# Hackaday 奖参赛作品:Vibhear

> 原文：<https://hackaday.com/2017/09/05/hackaday-prize-entry-vibhear/>

部分或全部听力障碍是困扰许多人的严重问题。全球近 5%的人口患有某种形式的听力障碍。对于那些从出生就受到这种残疾影响的人来说，它进一步影响了语言和言语能力的发展。近年来，人工耳蜗越来越多地用于解决这个问题。这些植入物由两部分组成——接收器和电极阵列植入耳朵附近的皮肤下(电极阵列终止于耳蜗内部)，而麦克风、电子设备、发射器和电源则附着在外部。通常，外部单元必须被移除——例如，当人需要睡觉时。对于幼儿来说尤其如此。与他们的头部相比，外部单元相当大，并在睡眠期间引起不适。家长们担心这个昂贵的设备会在孩子睡觉时被损坏。这导致了令人担忧的情况，即儿童睡着了，没有从周围环境接收到听觉输入。他们不仅听不到早晨的警报，而且在紧急情况下，如烟雾警报响起时，也无法做出反应。

【SRD Jan Pavlovic】当他拜访他的朋友并了解到他们六岁的儿子从出生起就失聪时，他直接遇到了这个问题。这对父母说，他们的孩子不会在晚上被噪音打扰，因为他的人工耳蜗的外部单元每天晚上都被移除。[Srdjan]然后开始制造[vib hear——一种辅助助听设备](https://hackaday.io/project/26277-vibhear),在主助听器被移除或不起作用时使用。这是一种低成本的臂带，可响应高环境噪音提供振动信号。

主要组件是麦克风、放大器、微控制器和振动电机，由 LiPo 电池通过升压转换器/充电器供电。RTC 模块允许设置每日唤醒警报。它目前是围绕 Arduino 的原型，但下一次迭代将使用一个专门的 DSP，可以对其进行编程，以对输入声音执行信号处理操作。这将允许识别特定的声音，如汽车喇叭、狗叫声、烟雾警报或紧急警报。

【SRD Jan】正在为他的下一次迭代选择元件，所以如果你有任何建议来帮助他选择微控制器、电源控制器或其他器件，请通过下面的评论告诉他。

The [HackadayPrize2017](https://hackaday.io/prize) is Sponsored by:[![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Texas Instruments](img/3734f1c96ffff85ea2a7eaddc92844ba.png)](https://hackaday.io/ti)