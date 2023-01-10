# 车库设计的故事:从不精确的部分实现精确

> 原文：<https://hackaday.com/2016/04/12/tales-of-garage-design-achieving-precision-from-imprecise-parts/>

设计完美匹配的零件很难。无论是我们制造工具的粗糙还是制造零件的供应商的程序，零件很少是我们希望的精确尺寸。可悲的是，这就是我们生活在现实世界中所付出的代价:没有我们的程序(甚至我们的测量工具！)都很完美。在一个由不完美的零件、不完美的程序和不完美的测量技术组成的世界里，我们究竟应该如何建造任何可以工作的东西呢？幸运的是，我们很幸运！从过去工程师沉思的头脑中，产生了一套设计技术，可以对抗生活在错误世界中的不完美。

## 在不重要的地方偷工减料的案例研究

为了给我们一些背景知识，我想我会尝试这些技术，同时建立一个 2 轴机架来移动激光切割机的光学系统。有什么问题吗？我离真正的机械商店很远，所以我用一个带锯、一个锯子、一个微型磨和一些测量工具工作。然而，好的设计实践仍然可以从少量的手工工具中获得。既然门架已经完成，我想我应该带我们进行一次设计之旅，看看我们如何在家里设计项目时“偷工减料”——而不会真正牺牲任何性能。

### 重要的是精度高于准确度

有时候，确定一个组件的精确尺寸没有组件之间的尺寸差异重要。如果我们自己制造这些零件，我们需要确保我们处理这些零件的程序尽可能地使它们接近相同。在激光切割机的情况下，框架成为一个伟大的候选人，以确保相关部分几乎相同的长度。

我承认，这个项目的设计阶段让我对一个可爱的 CAD 模型垂涎三尺。精确到 850.00 毫米的挤压管材模型…完美立方体的角撑模型…然而，制造这些零件来满足 CAD 对应的尺寸将是另一个考验。可悲的是，在切割挤出的管子之前，我所需要测量的不过是一把松软的卷尺。粗制滥造？是的，但是那样我可以得到大概的尺寸。幸运的是，设计一个工作的龙门框架背后的秘密是，满足这些管道的精确尺寸并不重要！重要的是在需要相同长度的零件之间实现紧密的*相对尺寸公差*。
![26200207041_af6a04e011_z](img/634ac482dd9184e2fdd16e6d74b3ebca.png)

让我们近距离观察一下龙门框架。红色长度为 850 毫米；绿色，600 毫米；和红色，160 毫米，根据 CAD 模型。用卷尺，我无法在这些尺寸的几毫米范围内做得更好。不过，没关系。只要同色的框管都尽可能的接近相同的长度，整体的框还是会是方的(…或者足够方)。我们如何确保紧密的相对尺寸精度？用胶带把它们粘在一起，同时把它们全切了！

### 不完善库存零件的核算

设计完美配合的零件很难，但真正完美的配合是不切实际的。事实上，工程师甚至不会在设计系统时假设他们的部件需要完美匹配。相反，他们会设计自己的零件来适应各种尺寸。工程学有一个可爱的词:公差。有时候是我:“我可以把那个洞钻成 8[毫米]正负 0.1[毫米]。”有时是数据表:“厚度为正负 0.05 英寸。”不管怎样，公差给了我们的尺寸一个范围。如果我们牢记这些公差，我们可以设计适应这些范围，使我们的零件即使尺寸略有偏差也能装配在一起。

作为一个例子，让我们看看一个步进电机通过一个同步带和两个滑轮驱动一个轴。根据制造商的说法，正时皮带有一个标称长度，由皮带的齿距和齿数决定。皮带轮也有一个标称尺寸，称为“节圆”，这是一个围绕齿的虚拟圆，我们可以假设皮带在这里运行。给定每个滑轮节圆的尺寸和皮带的标称长度，我们可以计算两个滑轮之间的间距。

![Image Credit: bepltd.com ](img/3ab00721832928b440553e9cb39abff0.png)

Image Credit: bepltd.com

不幸的是，正时皮带的长度往往会随着皮带的张力、温度和寿命而变化，因此预测皮带的*精确长度*是不实际的。幸运的是，我们不需要！牢记皮带长度的可变性，我们可以设计零件，通过一系列连接零件的设定点来适应这种可变性。

![26209752512_9ef8280562_z](img/7c1248c28ef542ce0890ae0302d5278b.png)

在激光切割机 X 轴的情况下，我将孔转换为皮带标称长度周围的槽。为了拉紧皮带，一旦电机与皮带接合，我可以简单地将电机拉下槽。总而言之，这条腰带有点短，不能假设它会显著拉伸。另一方面，电机槽在安装和拆卸过程中起到了第二个方便的作用。要移除马达，我可以将它向相反方向滑动，以释放张力。总而言之，这是一个非常简单的修改，但它解决了皮带张力问题，不需要任何花哨的皮带张紧器或额外的零件！

### 为校准而设计——然后校准

当我们设计电机板时，我们给了它一个标称长度，然后添加了一个上下范围，以考虑皮带拉伸和其他变化。我们可以把这个想法用于各种各样的配对零件。不幸的是，有时我们无法凭感觉找到两个部分相遇的确切位置。在这种情况下，我们需要更好的东西。我们需要更多的工具和技术来让一切都在正确的位置。

如今，大多数二氧化碳激光切割机使用一种叫做“飞行光学”的技术尽管名字很花哨，但这是一个非常简单的概念。不要在我们想要切割的表面上移动整个激光器，保持激光器固定，只是围绕光束移动。一个飞行的光学系统创造了奇迹，因为我们的机架电机只需要足够强大，以合理的加速度踢几个反弹镜，而不是整个管子。有什么问题吗？当我们第一次组装激光切割机时，据我们所知，从那台激光器发出的一次照射，我们就可以在旁边炸开一个洞，超出框架，进入邻居的院子！(说真的，各位，我们还是安全一点吧。)简而言之，光束的光路需要精确，其精度不可能来自设计本身。(我在车库里造这个，记得吗？)制造我们零件的机器并不完美，我们把这些零件拧在一起的粗糙的手也不完美。简而言之，我们不能保证零件将适合在正确的光束路径所需的准确位置。要造一台激光切割机，我们需要为对准而设计，然后对准它！我们的激光切割机制作伙伴通过将他们的反射镜安装在具有精细粒度的可调设定点的平台上来解决这些缺陷。在我的台架上，我安装了三个。

接下来是实际的对齐。抬头；激光是隐形的！它也很擅长烧毁任何挡在它路上的东西。没什么大不了的，对吧？(各位，请戴上安全眼镜！)首先，我用量角器粗略估计了一下 45 度，然后拧紧了镜板。从那里，我粗略地猜测了一下光束的路径，放了一张纸在路上，然后——噗——激光穿过了纸！在这一点上，开始调整每一面镜子，直到纸上的烧伤痕迹大致朝着镜子的方向移动。经过几轮噗的一声，我让激光大致着地了三面镜子。

最后一步，我需要对光束的真实位置有一个更好的猜测，然后我真正有洞的纸会告诉我。我需要那些镜子处于一个真正的 45 度角，而我车库里的任何测量工具都无法让我达到这个角度。比起试图依靠完美的镜面角度，[比我聪明得多的了不起的人们](http://hackaday.com/2016/03/10/aligning-invisible-lasers-on-the-cheap/)建议用可见的引导激光来欺骗激光的实际路径，所以这正是我所做的。在纸上画了几个烧痕后，我用激光笔追踪这些烧痕。从那里，我可以自信地预测光束路径，并将镜子调整到最终位置。

### 不精确零件的精密之旅

很快——这是一个由铝管、铝盘和一双猴手组成的工作激光切割机，用来将它们拧在一起！然而，有些事情很奇怪。公平地说，这些在锯床和铣床上制造的零件相当难看。孔洞过大。这些切口的表面光洁度是令人厌恶的。尽管有这些不完美的部分，使用适当的工具和技术进行调整，我仍然可以实现一个工作系统。准确度和精确度不是来自零件，而是用于最终将它们放在正确位置的工具和技术——留出余量。这是一个教训。

在现实世界中，没有什么是完美的。吉他弦必须调音。自行车刹车必须拉紧。尽管存在这些误差，但如果我们在设计器件时考虑到校准，只关注重要的尺寸，我们仍然可以将系统调整到工作状态。对于所有被困在现实世界中的人们，我们很想听听你们是如何在评论中调整设计的。