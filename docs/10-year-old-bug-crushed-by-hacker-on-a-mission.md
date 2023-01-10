# 10 岁的臭虫在一次任务中被黑客粉碎

> 原文：<https://hackaday.com/2017/10/31/10-year-old-bug-crushed-by-hacker-on-a-mission/>

PCI 直通是虚拟化客户系统直接访问 PCI 硬件的能力。专用 GPU 的直通最近刚刚被添加到基于 Linux 内核的虚拟机中。不久之后，用户开始发现，在嵌套页表(NPT)上切换，一种旨在为虚拟机提供硬件加速的技术，在 AMD 平台上产生了相反的效果，并将帧速率降至爬行。

对此[gnif] [很恼火，着手解决问题](https://lists.linuxfoundation.org/pipermail/iommu/2017-October/024823.html)。他的第一步是运行图形基准来隔离问题的根源。确定了 GPU 中的罪魁祸首后，[gnif]开始阅读相关的技术栈。花了三天时间研究技术文档，让[gnif]找到了导致内存设置错误的那一行代码，并实现了一个基本的修复。然后他把工作交给了 patchwork.kernel.org[的【保罗·邦兹尼】，后者发布了一个更完善的补丁。](https://patchwork.kernel.org/patch/10027523/)

影响 PCI 直通的错误已经存在了十年，但很少受到制造商的关注。当显卡受到影响时，它变得更加突出。最终，一个非常敬业的用户花了三天时间来修复它，然后又花了一天时间来为开源操作系统推出补丁。在他的笔记中[gnif]指出 AMDs 文档是多么有用。随着[维修权](https://hackaday.com/2017/10/02/a-bit-of-mainstream-coverage-for-the-right-to-repair/)的争论，DRMed 技术文档和标准被锁在付费墙后面，[gnif]的故事提醒人们可访问的质量文档的重要性。