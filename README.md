# Selorify 碎月
在Github上开一个仓库用来放之前写的碎月，来看更新会方便一点（）  
~放在这个上面本来应该开源了，但是我代码写得太烂了，等再过几个版本我改好一点再把源码放上来吧~
___
## 更新日志  
> 2026.6.8 v1.1.3rc
* 更新了版权声明
* 重构了对于PS的dat资源替换方法，大幅缩减了程序大小。然而，由于在真实使用中可能存在的情况太多，无法测试所有情况，虽然尽可能保证在正常使用的一般情况下结果尽可能完美，但是大概或许可能会在极端的边界情况下产生不那么完美的情况（尽管应该不会真的存在致命问题），因此建议如果需要对同一个目标多次修改，最好不要连续修改保存以后又继续修改保存非常多次，建议还原备份以后重新修改（尽管理论上最坏的情况可能只是导致资源文件一直变大，但是可能大概也许在某些情况下会导致问题？尽管或许不太可能？）
* 修复了对于PS 2025+资源替换会导致的错误（其实去年年底就发现这个问题并找到原因了，但是一直没时间改，现在基本修复了，但是还因为重构了对于PS的dat资源替换方法，所以可能对于旧版本会有影响，但是没时间全部测完，总体上应该是没有太大问题的，如果对于旧版本PS CC的修改存在问题的话可以尝试用v1.1.2b版本或者在github提交issue）
* 对部分软件的一部分较新版本提供了支持，目前支持的软件和版本范围：

|软件|版本范围|
|:-|:-|
|Adobe Photoshop|3.0-2026|
|Adobe After Effects|3.1、CS3-2026|
|Adobe Premiere Pro|CS6-2026|
|Adobe Premiere Rush|1.x-2.x(CC 2019-2025)|
|Adobe Audition|CS6-2026|
|Adobe Flash Professional|CS4-CC 2014|
|Adobe Animate|CC 2015-2024|
|Adobe Character Animator|2020-2026|
|Adobe Photoshop Lightroom|4-Classic (2026)|
|Adobe Illustrator|CS6-2026|
|Adobe InDesign|CS6-2026|
|Adobe InCopy|2020-2026|
|Adobe Media Encoder|CC 2014-2026|

截止当前版本发布时，An似乎尚未发布2025版本，已根据以往版本的启动界面命名规则进行了推测，因此有较大概率可以成功修改，但不保证一定成功，建议做好备份再尝试。

对于其中几个软件的较新版本，同时存在Drak和Light Splash，但是好像一直用的是Dark Splash，Light Splash似乎没有用？目前暂时没有研究具体有什么区别。

目前已知的问题（其实一直都有这个问题，但是其实不太能算是本程序导致的问题）：
* 如果修改后的图像和修改之前的**尺寸**差别非常大（如果是文件空间大小差距大的话好像没有太大的影响，未进行特别详细的测试），可能会导致目标崩溃，尽管尚未确定到底多大算“大”，似乎如果差别不是很大的话没有太大的问题。为了保留自由性，目前本程序没有对输入图像做大小限制，未来大概也不会加，请自行评估可行性。
* 如果目标位于需要管理员权限才能修改的目录，而未以管理员权限运行本程序，那么可能导致即便提示修改成功、预览看上去也是对的（目前不确定为什么会这样），但是实际上没有成功，因此如果存在该情况，建议以管理员身份运行本程序并重试。

> 2025.12.6 v1.1.2b
* 更新了使用许可和免责声明。移除旧版本下载链接，现在所有使用许可和免责声明以新版本为准。
* 增加了上一版本支持的软件的已经发布的2026版的支持（对于未发布2026版的，已在2025版进行测试，并使用推定的2026版资源名称尝试提供支持），目前支持的软件和版本范围：

|软件|版本范围|
|:-|:-|
|Adobe Photoshop|3.0-2026|
|Adobe After Effects|3.1、CS3-2025|
|Adobe Premiere Pro|CS6-2025|
|Adobe Audition|CS6-2025|
|Adobe Flash Professional|CS4-CC 2014|
|Adobe Animate|CC 2015-2024|
|Adobe Photoshop Lightroom|4-Classic (2026)|
|Adobe Illustrator|CS6-2026|
|Adobe InDesign|CS6-2026|
|Adobe Media Encoder|CC 2014-2025|

> 2022.11.2 v1.1.1  
* 增加了上一版本支持的软件的2023版的支持，目前支持的软件和版本范围：

|软件|版本范围|
|:-|:-|
|Adobe Photoshop|3.0-2023|
|Adobe After Effects|3.1、CS3-2023|
|Adobe Premiere Pro|CS6-2023|
|Adobe Audition|CS6-2023|
|Adobe Flash Professional|CS4-CC 2014|
|Adobe Animate|CC 2015-2023|
|Adobe Photoshop Lightroom|4-Classic (2023)|
|Adobe Illustrator|CS6-2023|
|Adobe InDesign|CS6-2023|
|Adobe Media Encoder|CC 2014-2023|


> 2022.8.26 v1.1  
* 增加了上一版本支持的软件的2022版的支持，并对Ps、Ae的一些远古版本提供了支持（某些老版本的安装包真的太难找了QAQ，比如Ps 2.0的，如果有这个资源的小伙伴能不能提供一份给我qwq）
* 修复了一些提示语  
* 一些细节的修改  
* 改了数据存的结构，所以我以后更新大概也许可能应该不会那么慢了x  
* __由于Windows的UIPI（用户界面特权隔离）的限制存在，以管理员身份运行程序时，向程序中拖拽文件识别可能会失效，出于安全考虑，
这个版本以及后续版本大概都不会去解决管理员模式下运行拖拽失效的问题，以管理员身份运行时还请手动选择目标位置__（不过一般来说大部分人大概也许可能不会把Adobe全家桶那么大的软件
装在C盘吧x，一般来说只要不在C盘基本上是不会出现权限问题的x）  
  
> 2021.2.23 v1.0
* 对以下软件提供支持：  
  
|软件|版本范围|
|:-|:-|
|Adobe Photoshop|CS2-2021|
|Adobe After Effects|CS4-2020|
|Adobe Premiere Pro|CS6-2020|
|Adobe Audition|CS6-2020|
|Adobe Flash Professional|CS4-CC 2014|
|Adobe Animate|CC 2015-2021|
|Adobe Photoshop Lightroom|4-Classic (2021)|
|Adobe Illustrator|CS6-2021|
|Adobe InDesign|CS6-2021|
|Adobe Media Encoder|CC 2014-2020|
___
## 软件介绍  
从多年前开始用Adobe的软件开始一直对修改它的启动界面念念不忘。现在网络上对于修改它启动界面的教程、工具都很多，像比如不知语冰老师的PsCoser，和比如moeen等
适用性很强的图片资源修改器以及诸如ResourceHacker等老牌的PE文件资源修改工具。诚然，这些工具都可以适用，但就个人修改经历来看，上述这些软件有的做的虽然确实
很不错，界面也非常好看，比如不知语冰老师的PscCoser，但似乎只专精于对于PsCC版本以后的修改，有时像改比如也很常用的CS6或是其他Adobe软件还是得求助于其他工具，
并且不知道是不是我没看到的问题，有时想保存读取出的原版Ps启动界面时没有找到直接的保存按钮有一点难受；而像其他的修改工具虽然可以修改的种类多了但又感觉缺少
像PsCoser一样的易用性。

基于以上几点，也是对多年前b站上发的一大堆以此相关的水的视频做个结尾，我开发了一个简便的可以完成Adobe个人觉得常用的设计类软件（Ps、Ai、Id、Lr、Fl（An）、
Pr、Ae、Au、Me）的覆盖常用全版本(CS6-2022)的快速修改启动画面的小工具，支持自动识别、保存、修改启动画面等功能。

同时也实现了良好的界面效果（虽然有点花里胡哨），实现了视差效果的界面、自动匹配win10主题颜色调整界面颜色，win10系统下的窗体背景亚克力效果（1809版本以下亚
克力效果会出现严重性能问题），以及兼容win7（需要.Net4.5.2支持，否则会报错），缺点就是cpu占用有那么一点点高xwx。
<p align="center">
<img src="https://github.com/DragonLingLuo/Selorify/blob/main/SampleImages/main.jpg" height="400">
<img src="https://github.com/DragonLingLuo/Selorify/blob/main/SampleImages/extendedMain.jpg" height="400">
<img src="https://github.com/DragonLingLuo/Selorify/blob/main/SampleImages/support.jpg" height="400">
</p>

（其实剩着的Dw、Fw、Dn等以及像Vegas、CorelDRAW等技术上实现是没有难度的，只是因为作者实在是没有时间，不过以后有时间应该会陆续更新支持）

（另外对于更古早版本的支持也还在更新，但是一方面因为我太忙了（所以1.1拖了这么久没更xwx），另一方面因为做这个要先找到支持的版本的资源文件，但是古早版本的安
装包太难找了，并且某些版本的资源有加密（比如Ae 6.0-7.0），得想办法先破解，所以进度比较慢）
___
## 其他信息
> 其他发布站点
>> 知乎：<https://www.zhihu.com/question/31515371/answer/1745727468>  
>> 蓝奏云：<https://wwbio.lanzoue.com/b0syqdmpe> 密码:82hb
>> Bilibili：不是很想放过来
  
> 联系作者
>> 请直接用github联系我  
>> 不会用github的可以发邮件：contact@lingluo.moe
