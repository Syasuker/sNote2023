# New courses on distributed systems and elliptic curve cryptography  
分布式系统和椭圆曲线密码学的新课程

Published by Martin Kleppmann on 18 Nov 2020.  
由马丁·克莱普曼于 2020 年 11 月 18 日发布。

I have just published new educational materials that might be of interest to computing people: a new 8-lecture course on distributed systems, and a tutorial on elliptic curve cryptography.  
我刚刚发布了计算人员可能感兴趣的新教育材料：关于分布式系统的新 8 个讲座课程，以及椭圆曲线密码学教程。

## Distributed Systems 分布式系统

Since last year I have been delivering an 8-lecture undergraduate course on distributed systems at the University of Cambridge. The first time I delivered it, I inherited the slides and exercises from the people who lectured it in previous years (Richard Mortier, Anil Madhavapeddy, Robert Watson, Jean Bacon, and Steven Hand), and I just used those materials with minor modifications. It was a good course, but it was getting quite dated (e.g. lots of material on [CORBA](https://en.wikipedia.org/wiki/Common_Object_Request_Broker_Architecture), which is now of mostly historical interest).  
自去年以来，我一直在剑桥大学开设一门关于分布式系统的8个讲座的本科课程。我第一次讲授它时，我继承了前几年讲课的人（Richard Mortier，Anil Madhavapeddy，Robert Watson，Jean Bacon和Steven Hand）的幻灯片和练习，我只是在稍作修改的情况下使用这些材料。这是一个很好的课程，但它已经过时了（例如，关于 CORBA 的大量材料，现在主要是历史兴趣）。

Therefore, this year I decided to do a thorough refresh of the course content, and wrote a brand new set of slides and lecture notes. Also, due to the pandemic we are not having any in-person lectures, so I recorded videos for all of the lectures. I decided to make all of this available publicly under a [creative commons CC BY-SA license](https://creativecommons.org/licenses/by-sa/4.0/), which means that you’re welcome to use it freely (including incorporating it into your own work), provided that you give credit to me, and that you share your derived work under the same license.  
因此，今年我决定对课程内容进行彻底的更新，并写了一套全新的幻灯片和讲义。此外，由于大流行，我们没有任何面对面的讲座，所以我为所有讲座录制了视频。我决定在知识共享CC BY-SA许可下公开提供所有这些内容，这意味着欢迎您自由使用它（包括将其合并到您自己的作品中），前提是您注明出处，并且您在同一许可下共享您的衍生作品。

The result is here:  
结果在这里：

- [Lecture notes (PDF)](https://www.cl.cam.ac.uk/teaching/2122/ConcDisSys/dist-sys-notes.pdf) (including exercises)  
    讲义 （PDF） （包括练习）
- Slides: [slideshow](https://www.cl.cam.ac.uk/teaching/2122/ConcDisSys/dist-sys-slides.pdf) and [printable](https://www.cl.cam.ac.uk/teaching/2122/ConcDisSys/dist-sys-handout.pdf) (PDF)  
    幻灯片：幻灯片和可打印 （PDF）
- [Lecture videos (YouTube)  
    讲座视频（优酷）](https://www.youtube.com/playlist?list=PLeKd45zvjcDFUEv_ohr_HdUFe97RItdiB)
- [Course web page 课程网页](https://www.cl.cam.ac.uk/teaching/2122/ConcDisSys/)
- Solution notes for the exercises are available on demand ([email me](https://martin.kleppmann.com/contact.html) and convince me that you’re not a student trying to cheat). Cambridge supervisors can [download the solution notes directly](https://www.cl.cam.ac.uk/teaching/2122/ConcDisSys/supervisors/dist-sys-solutions.pdf) (Raven login required).  
    练习的解决方案说明可按需提供（给我发电子邮件并说服我你不是试图作弊的学生）。剑桥主管可以直接下载解决方案说明（需要 Raven 登录）。

The course is primarily designed for Cambridge undergraduate students, and it includes some cross-references to other courses. Many other courses also make their notes or slides publicly available, so you can still look them up if you’re not at Cambridge by going to the [course web pages](https://www.cl.cam.ac.uk/teaching/2122/part1b.html). (Many lecturers restrict their video recordings to Cambridge users only, so those might not be publicly available.)  
该课程主要为剑桥本科生设计，包括对其他课程的一些交叉引用。许多其他课程也公开了他们的笔记或幻灯片，因此如果您不在剑桥，您仍然可以通过访问课程网页来查找它们。（许多讲师将他们的视频录制限制为剑桥用户，因此这些视频可能不会公开。

The distributed systems course comprises about 7 hours of video and 87 pages of lecture notes. It covers the following topics:  
分布式系统课程包括大约 7 小时的视频和 87 页的讲义。它涵盖以下主题：

1. Introduction: distributed systems, computer networks, and RPC  
    简介：分布式系统、计算机网络和 RPC
2. System models: network faults, crash and Byzantine faults, synchrony assumptions  
    系统模型：网络故障、崩溃和拜占庭故障、同步假设
3. Physical clocks, clock synchronisation, and causality  
    物理时钟、时钟同步和因果关系
4. Logical time, broadcast protocols (reliable, FIFO, causal, total order)  
    逻辑时间、广播协议（可靠、先进先出、因果关系、总阶数）
5. Replication, quorum protocols, state machine replication  
    复制、仲裁协议、状态机复制
6. Consensus, details on the Raft consensus algorithm  
    共识，关于 Raft 共识算法的详细信息
7. Replica consistency, two-phase commit, linearizability, eventual consistency  
    副本一致性、两阶段提交、线性化、最终一致性
8. Case studies: collaboration software, Google’s Spanner  
    案例研究：协作软件，谷歌的扳手

The main focus of this course is on understanding the algorithms and the principles that allow us to build robust and reliable distributed systems. It uses examples of practical systems as motivation, and the videos include a few live demos of real distributed systems in action. The aim is to convey the fundamentals without being excessively theoretical; there are a few mathematical proofs in the exercises, but most of the discussion is informal and example-based.  
本课程的主要重点是理解使我们能够构建健壮可靠的分布式系统的算法和原理。它使用实际系统的示例作为动力，视频包括一些真实分布式系统的现场演示。目的是传达基础知识，而不会过多的理论化;练习中有一些数学证明，但大多数讨论都是非正式的和基于示例的。

The level of this course is intended for second-year undergraduates. Our students at this level have reasonable fluency with mathematical notation, and some background in programming languages and operating systems, so that’s what this course assumes.  
本课程的水平适用于二年级本科生。我们这个级别的学生对数学符号有相当流利的了解，并且在编程语言和操作系统方面有一些背景，所以这就是本课程的假设。

## Elliptic Curve Cryptography  
椭圆曲线加密

Another document I’m releasing today is called [Implementing Curve25519/X25519: A Tutorial on Elliptic Curve Cryptography](https://martin.kleppmann.com/papers/curve25519.pdf). There’s no video for this one, just a 30-page PDF.  
我今天发布的另一个文档叫做实现 Curve25519/X25519：椭圆曲线加密教程。这个没有视频，只有一个30页的PDF。

Many textbooks cover the concepts behind Elliptic Curve Cryptography (ECC), but few explain how to go from the equations to a working, fast, and secure implementation. On the other hand, while the code of many cryptographic libraries is available as open source, it can be [rather opaque to the untrained eye](https://github.com/jedisct1/libsodium/blob/master/src/libsodium/crypto_scalarmult/curve25519/ref10/x25519_ref10.c#L91-L132), and it is rarely accompanied by detailed documentation explaining how the code came about and why it is correct.  
许多教科书涵盖了椭圆曲线密码学（ECC）背后的概念，但很少有教科书解释如何从方程到工作，快速和安全的实现。另一方面，虽然许多加密库的代码是开源的，但对于未经训练的人来说，它可能相当不透明，并且很少附有详细的文档来解释代码是如何产生的以及为什么它是正确的。

This tutorial bridges the gap between the mathematics and implementation of elliptic curve cryptography. It is written for readers who are new to cryptography, and it assumes no more mathematical background than most undergraduate computer science courses. Starting from first principles, this document shows how to derive every line of code in an implementation of the [X25519](https://tools.ietf.org/html/rfc7748) Diffie-Hellman key agreement scheme, based on the [widely-used Curve25519 elliptic curve](https://ianix.com/pub/curve25519-deployment.html). The implementation is based on Dan Bernstein et al.’s [TweetNaCl](https://tweetnacl.cr.yp.to/). It is fast and secure; in particular, it uses constant-time algorithms to prevent side-channel attacks.  
本教程弥合了椭圆曲线密码学的数学和实现之间的差距。它是为刚接触密码学的读者写的，它没有比大多数本科计算机科学课程更多的数学背景。本文档从第一原则开始，介绍如何基于广泛使用的 Curve25519 椭圆曲线，在实现 X25519 Diffie-Hellman 密钥协议方案时派生每一行代码。该实现基于Dan Bernstein等人的TweetNaCl。它快速且安全;特别是，它使用恒定时间算法来防止侧信道攻击。

I wrote this because I wanted to learn how real implementations of ECC work, but I couldn’t find good resources that explained it, so I wrote the document as I figured it out step-by-step from a number of sources (and by doing a lot of the calculations myself). I hope others will also find it useful.  
我写这篇文章是因为我想了解 ECC 的实际实现是如何工作的，但我找不到好的资源来解释它，所以我写了这个文档，因为我从许多来源逐步弄清楚它（并通过自己做了很多计算）。我希望其他人也会发现它有用# 
   New courses on distributed systems and elliptic curve cryptography — Martin Kleppmann’s blog --- 分布式系统和椭圆曲线密码学的新课程 — Martin Kleppmann 的博客          
[Skip to content跳到内容](https://martin.kleppmann.com/2020/11/18/distributed-systems-and-elliptic-curves.html#content) 

** [Martin Kleppmann 马丁·克莱普曼](https://martin.kleppmann.com/)** 

* [About/Contact 关于/联系](https://martin.kleppmann.com/contact.html)
* [Supporters 支持者](https://martin.kleppmann.com/supporters.html)

⠀
---

# New courses on distributed systems and elliptic curve cryptography
# 分布式系统和椭圆曲线密码学的新课程

Published by Martin Kleppmann on 18 Nov 2020.
由马丁·克莱普曼于 2020 年 11 月 18 日发布。

I have just published new educational materials that might be of interest to computing people: a new 8-lecture course on distributed systems, and a tutorial on elliptic curve cryptography.
我刚刚发布了计算人员可能感兴趣的新教育材料：关于分布式系统的新 8 个讲座课程，以及椭圆曲线密码学教程。

## Distributed Systems 分布式系统

Since last year I have been delivering an 8-lecture undergraduate course on distributed systems at the University of Cambridge. The first time I delivered it, I inherited the slides and exercises from the people who lectured it in previous years (Richard Mortier, Anil Madhavapeddy, Robert Watson, Jean Bacon, and Steven Hand), and I just used those materials with minor modifications. It was a good course, but it was getting quite dated (e.g. lots of material on [CORBA](https://en.wikipedia.org/wiki/Common_Object_Request_Broker_Architecture), which is now of mostly historical interest).
自去年以来，我一直在剑桥大学开设一门关于分布式系统的8个讲座的本科课程。我第一次讲授它时，我继承了前几年讲课的人（Richard Mortier，Anil Madhavapeddy，Robert Watson，Jean Bacon和Steven Hand）的幻灯片和练习，我只是在稍作修改的情况下使用这些材料。这是一个很好的课程，但它已经过时了（例如，关于 CORBA 的大量材料，现在主要是历史兴趣）。

Therefore, this year I decided to do a thorough refresh of the course content, and wrote a brand new set of slides and lecture notes. Also, due to the pandemic we are not having any in-person lectures, so I recorded videos for all of the lectures. I decided to make all of this available publicly under a [creative commons CC BY-SA license](https://creativecommons.org/licenses/by-sa/4.0/), which means that you’re welcome to use it freely (including incorporating it into your own work), provided that you give credit to me, and that you share your derived work under the same license.
因此，今年我决定对课程内容进行彻底的更新，并写了一套全新的幻灯片和讲义。此外，由于大流行，我们没有任何面对面的讲座，所以我为所有讲座录制了视频。我决定在知识共享CC BY-SA许可下公开提供所有这些内容，这意味着欢迎您自由使用它（包括将其合并到您自己的作品中），前提是您注明出处，并且您在同一许可下共享您的衍生作品。

The result is here:
结果在这里：

* [Lecture notes (PDF)](https://www.cl.cam.ac.uk/teaching/2122/ConcDisSys/dist-sys-notes.pdf) (including exercises)
* 讲义 （PDF） （包括练习）
* Slides: [slideshow](https://www.cl.cam.ac.uk/teaching/2122/ConcDisSys/dist-sys-slides.pdf) and [printable](https://www.cl.cam.ac.uk/teaching/2122/ConcDisSys/dist-sys-handout.pdf) (PDF)
* 幻灯片：幻灯片和可打印 （PDF）
* [Lecture videos (YouTube)讲座视频（优酷）](https://www.youtube.com/playlist?list=PLeKd45zvjcDFUEv_ohr_HdUFe97RItdiB)
* [Course web page 课程网页](https://www.cl.cam.ac.uk/teaching/2122/ConcDisSys/)
* Solution notes for the exercises are available on demand ([email me](https://martin.kleppmann.com/contact.html) and convince me that you’re not a student trying to cheat). Cambridge supervisors can [download the solution notes directly](https://www.cl.cam.ac.uk/teaching/2122/ConcDisSys/supervisors/dist-sys-solutions.pdf) (Raven login required).
* 练习的解决方案说明可按需提供（给我发电子邮件并说服我你不是试图作弊的学生）。剑桥主管可以直接下载解决方案说明（需要 Raven 登录）。

⠀
The course is primarily designed for Cambridge undergraduate students, and it includes some cross-references to other courses. Many other courses also make their notes or slides publicly available, so you can still look them up if you’re not at Cambridge by going to the [course web pages](https://www.cl.cam.ac.uk/teaching/2122/part1b.html). (Many lecturers restrict their video recordings to Cambridge users only, so those might not be publicly available.)
该课程主要为剑桥本科生设计，包括对其他课程的一些交叉引用。许多其他课程也公开了他们的笔记或幻灯片，因此如果您不在剑桥，您仍然可以通过访问课程网页来查找它们。（许多讲师将他们的视频录制限制为剑桥用户，因此这些视频可能不会公开。

The distributed systems course comprises about 7 hours of video and 87 pages of lecture notes. It covers the following topics:
分布式系统课程包括大约 7 小时的视频和 87 页的讲义。它涵盖以下主题：

1. Introduction: distributed systems, computer networks, and RPC
1. 简介：分布式系统、计算机网络和 RPC
2. System models: network faults, crash and Byzantine faults, synchrony assumptions
2. 系统模型：网络故障、崩溃和拜占庭故障、同步假设
3. Physical clocks, clock synchronisation, and causality
3. 物理时钟、时钟同步和因果关系
4. Logical time, broadcast protocols (reliable, FIFO, causal, total order)
4. 逻辑时间、广播协议（可靠、先进先出、因果关系、总阶数）
5. Replication, quorum protocols, state machine replication
5. 复制、仲裁协议、状态机复制
6. Consensus, details on the Raft consensus algorithm
6. 共识，关于 Raft 共识算法的详细信息
7. Replica consistency, two-phase commit, linearizability, eventual consistency
7. 副本一致性、两阶段提交、线性化、最终一致性
8. Case studies: collaboration software, Google’s Spanner
8. 案例研究：协作软件，谷歌的扳手

⠀
The main focus of this course is on understanding the algorithms and the principles that allow us to build robust and reliable distributed systems. It uses examples of practical systems as motivation, and the videos include a few live demos of real distributed systems in action. The aim is to convey the fundamentals without being excessively theoretical; there are a few mathematical proofs in the exercises, but most of the discussion is informal and example-based.
本课程的主要重点是理解使我们能够构建健壮可靠的分布式系统的算法和原理。它使用实际系统的示例作为动力，视频包括一些真实分布式系统的现场演示。目的是传达基础知识，而不会过多的理论化;练习中有一些数学证明，但大多数讨论都是非正式的和基于示例的。

The level of this course is intended for second-year undergraduates. Our students at this level have reasonable fluency with mathematical notation, and some background in programming languages and operating systems, so that’s what this course assumes.
本课程的水平适用于二年级本科生。我们这个级别的学生对数学符号有相当流利的了解，并且在编程语言和操作系统方面有一些背景，所以这就是本课程的假设。

## Elliptic Curve Cryptography
## 椭圆曲线加密

Another document I’m releasing today is called [Implementing Curve25519/X25519: A Tutorial on Elliptic Curve Cryptography](https://martin.kleppmann.com/papers/curve25519.pdf). There’s no video for this one, just a 30-page PDF.
我今天发布的另一个文档叫做实现 Curve25519/X25519：椭圆曲线加密教程。这个没有视频，只有一个30页的PDF。

Many textbooks cover the concepts behind Elliptic Curve Cryptography (ECC), but few explain how to go from the equations to a working, fast, and secure implementation. On the other hand, while the code of many cryptographic libraries is available as open source, it can be [rather opaque to the untrained eye](https://github.com/jedisct1/libsodium/blob/master/src/libsodium/crypto_scalarmult/curve25519/ref10/x25519_ref10.c#L91-L132), and it is rarely accompanied by detailed documentation explaining how the code came about and why it is correct.
许多教科书涵盖了椭圆曲线密码学（ECC）背后的概念，但很少有教科书解释如何从方程到工作，快速和安全的实现。另一方面，虽然许多加密库的代码是开源的，但对于未经训练的人来说，它可能相当不透明，并且很少附有详细的文档来解释代码是如何产生的以及为什么它是正确的。

This tutorial bridges the gap between the mathematics and implementation of elliptic curve cryptography. It is written for readers who are new to cryptography, and it assumes no more mathematical background than most undergraduate computer science courses. Starting from first principles, this document shows how to derive every line of code in an implementation of the [X25519](https://tools.ietf.org/html/rfc7748) Diffie-Hellman key agreement scheme, based on the [widely-used Curve25519 elliptic curve](https://ianix.com/pub/curve25519-deployment.html). The implementation is based on Dan Bernstein et al.’s [TweetNaCl](https://tweetnacl.cr.yp.to/). It is fast and secure; in particular, it uses constant-time algorithms to prevent side-channel attacks.
本教程弥合了椭圆曲线密码学的数学和实现之间的差距。它是为刚接触密码学的读者写的，它没有比大多数本科计算机科学课程更多的数学背景。本文档从第一原则开始，介绍如何基于广泛使用的 Curve25519 椭圆曲线，在实现 X25519 Diffie-Hellman 密钥协议方案时派生每一行代码。该实现基于Dan Bernstein等人的TweetNaCl。它快速且安全;特别是，它使用恒定时间算法来防止侧信道攻击。

I wrote this because I wanted to learn how real implementations of ECC work, but I couldn’t find good resources that explained it, so I wrote the document as I figured it out step-by-step from a number of sources (and by doing a lot of the calculations myself). I hope others will also find it useful.
我写这篇文章是因为我想了解 ECC 的实际实现是如何工作的，但我找不到好的资源来解释它，所以我写了这个文档，因为我从许多来源逐步弄清楚它（并通过自己做了很多计算）。我希望其他人也会发现它有用。

If you found this post useful, please [support me on Patreon](https://www.patreon.com/martinkl) so that I can write more like it!
如果你觉得这篇文章有用，请在 Patreon 上支持我，这样我就可以写更多类似的文章！

To get notified when I write something new, [follow me on Mastodon](https://nondeterministic.computer/@martin) or [Twitter](https://twitter.com/martinkl), or enter your email address: 
要在我写新内容时收到通知，请在Mastodon或Twitter上关注我，或输入您的电子邮件地址：

I won't give your address to anyone else, won't send you any spam, and you can unsubscribe at any time. [🔄  ❓]()

## Subscribe[🔄  ❓]()

 [Site RSS feed 🔄  ❓](http://feeds.feedburner.com/martinkl)  

To find out when I write something new, sign up to receive an [email notification](https://martinkl.substack.com/), [follow me on Mastodon](https://nondeterministic.computer/@martin) or [Twitter](https://twitter.com/martinkl), or subscribe to the [RSS feed](http://feeds.feedburner.com/martinkl). [🔄  ❓]()

I won't give your email address to anyone else, won't send you any spam, and you can unsubscribe at any time. [🔄  ❓]()

## My book[🔄  ❓]()

 ![](book-cover-small.png) 

My book, [*Designing Data-Intensive Applications*](http://dataintensive.net), has received [thousands](https://www.goodreads.com/book/show/23466395-designing-data-intensive-applications) of five-star reviews.
我的书《设计数据密集型应用程序》收到了数千条五星评价。

I am a researcher working on [local-first software](https://www.inkandswitch.com/local-first/) and security protocols at [TU Munich](https://www.in.tum.de/en/in/cover-page/). If you find my work useful, please [support me on Patreon](https://www.patreon.com/martinkl).
我是慕尼黑工业大学本地优先软件和安全协议的研究员。如果你觉得我的工作有用，请在 Patreon 上支持我。

## Recent posts 最近的帖子

* 12 Oct 2022: [Verifying distributed systems with Isabelle/HOL](https://martin.kleppmann.com/2022/10/12/verifying-distributed-systems-isabelle.html)
* 2022 年 10 月 12 日：使用 Isabelle/HOL 验证分布式系统
* 03 Jan 2022: [Book Review: The Future of Fusion Energy](https://martin.kleppmann.com/2022/01/03/future-of-fusion-energy.html)
* 2022年1月3日：书评：聚变能源的未来
* 01 Sep 2021: [Several podcast interviews](https://martin.kleppmann.com/2021/09/01/podcast-interviews.html)
* 2021 年 9 月 1 日：几次播客采访
* 14 Apr 2021: [It's time to say goodbye to the GPL](https://martin.kleppmann.com/2021/04/14/goodbye-gpl.html)
* 2021 年 4 月 14 日：是时候告别 GPL 了
* 23 Feb 2021: [Building the future of computing, with your help](https://martin.kleppmann.com/2021/02/23/patreon.html)
* 2021 年 2 月 23 日：在您的帮助下构建计算的未来
* [Full archive 完整存档](https://martin.kleppmann.com/archive.html)

⠀
## Conference talks 会议会谈

* [22 Sep 2023 at Strange Loop22 Sep 2023 在 奇怪的循环](https://martin.kleppmann.com/2023/09/22/strange-loop.html)
* [29 Jun 2023 at GOTO Amsterdam2023年6月29日于阿姆斯特丹GOTO](https://martin.kleppmann.com/2023/06/29/goto-amsterdam.html)
* [28 Jun 2023 at Amsterdam |> Elixir2023年6月28日在阿姆斯特丹 |> 长生不老药](https://martin.kleppmann.com/2023/06/28/amsterdam-elixir.html)
* [29 Apr 2022 at Have You Tried Rubbing A Database On It? (HYTRADBOI)29 Apr 2022 在 您是否尝试过在其上摩擦数据库？（海特拉博伊）](https://martin.kleppmann.com/2022/04/29/hytradboi.html)
* [05 Apr 2022 at 9th Workshop on Principles and Practice of Consistency for Distributed Data (PaPoC)2022年4月5日，在第9届分布式数据一致性原则与实践研讨会（PaPoC）上](https://martin.kleppmann.com/2022/04/05/bft-crdt-papoc.html)
* [Full archive 完整存档](https://martin.kleppmann.com/talks.html)

⠀
---

 ![](creative-commons.png)  Unless otherwise specified, all content on this site is licensed under a [Creative Commons Attribution 3.0 Unported License](http://creativecommons.org/licenses/by/3.0/). Theme borrowed from [Carrington](http://carringtontheme.com), ported to [Jekyll](https://github.com/mojombo/jekyll) by Martin Kleppmann. [🔄  ❓]()

×翻译服务或网络似乎出了点问题...
Extension context invalidated.
关闭重试全部错误段落

[martin.kleppmann.com](https://martin.kleppmann.com/2020/11/18/distributed-systems-and-elliptic-curves.html)。