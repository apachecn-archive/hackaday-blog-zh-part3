# 用音频效果篡改图像

> 原文：<https://hackaday.com/2017/04/16/mangling-images-with-audio-effects/>

有没有想过，如果你用 Proco RAT 或 Boss Overdrive 浏览你在巴黎旅行时拍的那些快照会是什么样子？BF-3 侧翼怎么样？[Robert Foss]写了这个[漂亮的小脚本](https://github.com/robertfoss/audio_shop/) (GitHub) [，它可以像处理音频文件一样处理图像](http://memcpy.io/audio-editing-images.html)，这样你就可以在不投资一系列模拟踏板的情况下进行试验。测试您的音频/视频 DSP 直觉，看看您是否能在不看效果的情况下说出图像的名称。

如果你了解你的 Linux 命令行工具，这其实没什么大不了的——向下滚动到脚本的最底部，看看它是怎么做的。 [ffmpeg](http://ffmpeg.org/) 将图像转换为 YUV 格式，这比音频处理的 RGB 格式好得多，然后 [sox](http://sox.sourceforge.net/) 添加音频效果。通过 ffmpeg 的另一次旅行让你回到图像或视频。

好吧，这是作弊，因为它在电脑内部应用音频效果，但没有什么能阻止你实际上把音频拿出来，让它通过那个布满灰尘的小石头。当然，一旦你有了电脑之外的音频，世界就是你的了。重温辉煌的 70 年代，当时视频艺术家使用[增强的音频合成器](https://en.wikipedia.org/wiki/Video_synthesizer)制作作品。如果你还没有看过 [Sandin 图像处理器](http://www.audiovisualizers.com/toolshak/vidsynth/sandin/sandin.htm)或 [Scanimate](https://en.wikipedia.org/wiki/Scanimate) 的运行，你就得[做一些 YouTube 制作](https://www.youtube.com/watch?v=UHjkMThH0aE)。