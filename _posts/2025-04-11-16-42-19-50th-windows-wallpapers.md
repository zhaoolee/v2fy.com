---
title: 比尔盖茨庆祝微软50周年回忆博客（附原文翻译以及Windows纪念壁纸下载）
tags:
- 个人成长
categories:
- 杂谈
---





![](https://cdn.fangyuanxiaozhan.com/assets/17443684357347PDbbyyD.png)

今年是微软诞生50周年，比尔盖茨写了这篇回忆文章，介绍了他怎么会创立这家公司，文末给出了微软第一个产品 Altair BASIC 的PDF版源码以及纪念壁纸的下载地址

Celebrate 50 years of Microsoft with the company’s original source code

原文链接：https://www.gatesnotes.com/meet-bill/source-code/reader/microsoft-original-source-code

文章所在的网站为「盖茨笔记  gatesnotes.com」，里面的网页内容用了很炫酷的特效（防爬虫效果很好），普通的翻译软件翻译的排版效果很差，本篇文章直接对照图文做一下翻译，也写一些个人思考，算是抛玉引砖，雅俗共赏。



![](https://cdn.fangyuanxiaozhan.com/assets/1744534538315Ntwym145.png)

>  在微软公司发布Office, Windows95, Xbox, AI 之前，有一款产品，名为「阿尔泰  BASIC」



![](https://cdn.fangyuanxiaozhan.com/assets/1744534932912x2CeQMwf.png)



## 我写过的最酷的代码

> 1975年，我和保罗·艾伦创建了微软，因为我们相信我们的愿景：每张桌子上，每个家庭中都有一台计算机。

>  五十年后的今天，微软继续创新，寻找让生活更轻松、工作更高效的新方式。能够走过50年是一个巨大的成就，我们无法完成这一切，没有像史蒂夫·巴尔默和萨提亚·纳德拉这样的杰出领导人，以及曾在微软工作的许多员工。

> 虽然我很高兴庆祝这一周年纪念，但达到这一里程碑的同时，也有些许苦涩。我总是喜欢回顾微软的历史，幻想它的未来。但也很难相信，像我生命中如此重要的一部分，已经存在了半个世纪！

> 就像昨天一样，保罗和我还在哈佛的计算机实验室里，趴在PDP-10旁，写下将成为我们公司第一款产品的代码。



图片左侧的杂志内容来自《Popular Electronics》（《大众电子》）杂志。这是1975年1月的刊物，其中的一篇文章介绍了“Altair 8800”——一款由MITS公司生产的微型计算机。比尔·盖茨和保罗·艾伦正是因为这台计算机而深受启发，并决定为其开发BASIC编程语言的解释器，这也是微软创立的起点。

这篇文章标志着一个历史性的时刻，可以说它间接推动了微软的诞生，因此盖茨在图文中提到这本杂志封面对他产生了深远的影响。这也是盖茨回顾自己与保罗·艾伦共同创办微软的初衷之一。

现在计算机纸质杂志基本越来越少，不过倒也有平替，比如 https://news.ycombinator.com/



![](https://cdn.fangyuanxiaozhan.com/assets/1744535778773fKPxETR0.png)



>  那段代码一直是我写过的最酷的代码，直到今天你都可以在本页底部看到它。

> 微软的故事从一件事开始，那就是一本杂志。1975年1月的《Popular Electronics》杂志封面上展示了Altair 8800。Altair 8800是由一家名为MITS的小电子公司创造的，它是一个开创性的个人计算机套件，承诺将计算机技术带给爱好者。当保罗和我看到这个封面时，我们知道两件事：个人电脑革命即将到来，我们想要在这个行业的起点抓住机会。

> 当时，个人计算机几乎是不存在的。保罗和我知道，创造能够让人们编程Altair的软件，可以革新人们与这些机器的互动方式。所以，我们联系了MITS的创始人Ed Roberts，并告诉他，我们有一版可以让Altair 8800运行的BASIC编程语言。

> 问题只有一个：我们并没有这段代码。

> 我们得开始动手工作了。

很经典的创业操作，先联系对方，说自己有对方需要的商品，如果对方愿意沟通，就做一个出来。

![](https://cdn.fangyuanxiaozhan.com/assets/1744536028398KMTeAFYx.png)



> BASIC语言的基础

> 1964年，两位达特茅斯学院的教授发明了BASIC，旨在让没有计算机经验的人易于学习。只需少量的学习或技术能力，任何人都可以用BASIC编写自己的软件——从支票簿平衡程序到井字游戏都可以。BASIC是保罗和我学到的第一门语言（直到今天仍在使用）。

> 计算机语言如BASIC与英语或任何其他语言的作用相同。就像你可以用英语在咖啡馆点咖啡一样，你也可以用BASIC告诉计算机运行程序、解决数学问题或执行其他任务。

编程技术也是向着越来越简单的方向发展，屏蔽越来越多的底层细节，Java屏蔽了跨平台的复杂性，Python屏蔽了占据不同字节数的变量差异，AI屏蔽了编程语言本身的存在。



![](https://cdn.fangyuanxiaozhan.com/assets/1744536193579GnpDH2iJ.png)



> 翻译BASIC

> 有一个问题：计算机不讲BASIC语言。它们讲的语言复杂且不直观，编程非常困难。为了弥补这一差距，保罗和我决定创建一个BASIC解释器，它能在程序运行时逐行将代码翻译成计算机能够理解的指令。

> 我们曾考虑过创建一个类似的工具，叫做编译器，它将整个程序翻译并一次性运行。但我们认为，逐行解释器的方法对于初学者来说会更有帮助，因为它能够即时反馈代码，帮助程序员在出现错误时立即修正。

> 没有什么比当你发现自己的方法有效时更好的感觉了。



程序员都是懒人，越好用，越流行；Python和JavaScript这两种极其流行的编程语言，也是直接把代码丢给解释器，让编码步骤变得更简单，好用的东西，才更容易流行起来。

![](https://cdn.fangyuanxiaozhan.com/assets/1744370192733dsYft16d.png)



> 我一直是一个非常优秀的数学学生，发现数学中所需的逻辑和问题解决能力帮助我学习了计算机编程。



![](https://cdn.fangyuanxiaozhan.com/assets/1744536385973MAYW4EPJ.png)

> 保罗和我与Ric Weiland一起上学，后来他成为了微软的第二位员工。

![](https://cdn.fangyuanxiaozhan.com/assets/1744536486522CJmjRQkf.png)

> 开始行动!

> 保罗和我决定分头进行。我们没有Altair计算机所使用的Intel 8080芯片，因此保罗开始编写一个程序，用来模拟哈佛的PDP-10主机上的Altair。这让我们可以在没有真正Altair的情况下测试我们的软件。同时，我专注于编写主程序代码，另一位朋友Monte Davidjoff则负责编写名为数学包的一部分。我们日以继夜地编写了两个月，最终完成了我们所说已经存在的软件。

早期团队解决问题的能力很强，没有机器就自己写个模拟器，分工也明确，执行力也强，用时两个月，终于把东西做出来了（开始向对方说有现成的软件，然后拖了两个月，盖茨是不是需要每周拿着PPT，给对方加大药量）



![](https://cdn.fangyuanxiaozhan.com/assets/1744536639625KmenkBwM.png)

> 克服障碍

> 当时计算机内存非常昂贵。Altair的额外内存成本可能比计算机本身还贵，因此每一字节都非常重要。我们认为，如果能将我们的BASIC代码缩小到只有四千字节，那么Altair的用户仍然有足够的内存来运行他们编写的程序（而不必花费大量的额外钱）。

> 为了符合限制，我使用了各种技术来优化内存使用，例如紧凑的数据结构和高效的算法。这是一个有趣的挑战，保罗和我都很紧张，希望尽快搞定，将Altair BASIC送到MITS，当我在弄清楚一切，并让它顺利运行时，真的非常爽。

计算资源永远是不够用的，开发者需要不断优化程序，这就是钻研数据结构和算法的价值；对应到2023年，大模型的显存占用恐怖的很，显存又贵的很，模型厂商的策略是不断优化基础模型，推出不同参数量的版本，让用户以更低的成本运行程序。

![](https://cdn.fangyuanxiaozhan.com/assets/1744536800044pG0PPJDR.png)

> 微软的诞生

> 最后，在经历了无数个不眠之夜后，我们准备向MITS的总裁Ed Roberts展示我们的BASIC解释器。演示非常成功，MITS同意授权这款软件。这是保罗和我公司创立的一个重要时刻，我们决定将其命名为Micro-Soft。（后来我们去掉了连字符。）

> 你可以在我的回忆录《源代码》中了解到更多关于Altair BASIC的起源——包括保罗如何在飞往阿尔伯克基的航班上完成部分代码。

> 想想看，这一小段代码是如何引领微软走向半个世纪的创新的，真是令人惊讶。在Office、Windows 95、Xbox或AI之前，就有了这段源代码——即使到现在，我看到它仍然会感到很兴奋。



Micro命名的初衷应该是指软件很小，运行很高效。虽然愿景是好的，但现在微软的office和Windows为了兼容上古软件的运行，真的大到离谱；

按照盖茨对于Basic解释器的想法，要为用户提供简单的使用体验，用户确实获得了在Win11运行Win98软件的简单，代价就是无比巨大的软件体积。

当然微软还是和腾讯没得比，腾讯云的SDK都能100MB起步！

![](https://cdn.fangyuanxiaozhan.com/assets/1744539149322Fmd1d8mN.png)

![](https://cdn.fangyuanxiaozhan.com/assets/1744536891501NjXwRQKf.png)



源代码地址：https://images.gatesnotes.com/12514eb8-7b51-008e-41a9-512542cf683b/34d561c8-cf5c-4e69-af47-3782ea11482e/Original-Microsoft-Source-Code.pdf



![Microsoft_50th_Mahjong_Dark_4k](https://cdn.fangyuanxiaozhan.com/assets/1744368674013PRSbdR8y.jpeg)

![Microsoft_50th_Mahjong_Dark_Wide](https://cdn.fangyuanxiaozhan.com/assets/1744368673936YdRcnQid.jpeg)

![Microsoft_50th_Mahjong_Light_Wide](https://cdn.fangyuanxiaozhan.com/assets/1744368674047ftdM8AD5.jpeg)

![Microsoft_50th_Solitaire_Dark_Wide](https://cdn.fangyuanxiaozhan.com/assets/17443686740927SiPETr4.jpeg)

![Microsoft_50th_Solitaire_Light_Wide](https://cdn.fangyuanxiaozhan.com/assets/1744368674007MhwfZNj2.jpeg)

![Microsoft_50th_Tulips_Dark_4k](https://cdn.fangyuanxiaozhan.com/assets/1744368673879Xmz4yWwS.jpeg)

![Microsoft_50th_Mahjong_Light_4k](https://cdn.fangyuanxiaozhan.com/assets/174436867413820fDiNEA.jpeg)

![Microsoft_50th_Solitaire_Dark_4k](https://cdn.fangyuanxiaozhan.com/assets/1744368674153M2SzbZfr.jpeg)

![Microsoft_50th_Solitaire_Light_4k](https://cdn.fangyuanxiaozhan.com/assets/1744368674202jW1PrfCz.jpeg)

![Microsoft_50th_Tulips_Dark_Wide](https://cdn.fangyuanxiaozhan.com/assets/1744368674158mzySPXAQ.jpeg)

![Microsoft_50th_Tulips_Light_4k](https://cdn.fangyuanxiaozhan.com/assets/1744368674186K42fdDHT.jpeg)

![Microsoft_50th_Tulips_Light_Wide](https://cdn.fangyuanxiaozhan.com/assets/1744368673929KK42MHnb.jpeg)

![Microsoft_50th_Windows_Dark_4k](https://cdn.fangyuanxiaozhan.com/assets/1744368673785fRp8s5x7.jpeg)

![Microsoft_50th_Windows_Dark_Wide](https://cdn.fangyuanxiaozhan.com/assets/1744368674002tmmdFms6.jpeg)

![Microsoft_50th_Windows_Light_4k](https://cdn.fangyuanxiaozhan.com/assets/1744368674352Yb8RrdsT.jpeg)

![Microsoft_50th_Windows_Light_Wide](https://cdn.fangyuanxiaozhan.com/assets/1744368674162EdAhrwGa.jpeg)

五十周年纪念壁纸下载地址：https://unlocked.microsoft.com/wp-content/uploads/2025/03/50th-windows-wallpapers.zip
