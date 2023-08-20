---
# multilingual page pair id, this must pair with translations of this page. (This name must be unique)
lng_pair: post_20230802
title: "Epigenetics and Chromatin Biology Conference."

# post specific
# if not specified, .name will be used from _data/owner/[language].yml
author: Zhenyu Liu
# multiple category is not supported
category: Work
# multiple tag entries are possible
tags: [Meeting]
# thumbnail image for post
img: ":post_20230819/cover.jpeg"
# disable comments on this page
comments_disable: true

# publish date
date: 2023-08-19 08:11:06 +0900

# seo
# if not specified, date will be used.
#meta_modify_date: 2022-02-10 08:11:06 +0900
# check the meta_common_description in _data/owner/[language].yml
#meta_description: ""

# optional
# if you enabled image_viewer_posts you don't need to enable this. This is only if image_viewer_posts = false
#image_viewer_on: true
# if you enabled image_lazy_loader_posts you don't need to enable this. This is only if image_lazy_loader_posts = false
#image_lazy_loader_on: true
# exclude from on site search
#on_site_search_exclude: true
# exclude from search engines
#search_engine_exclude: true
# to disable this page, simply set published: false or delete this file
#published: false
---

<!-- outline-start -->

Things learned from attending meetings Epigenetics and Chromatin Biology Conference in Wuhan.

<!-- outline-end -->

入学两年来头一次出去参加线下会议！这次是回武汉参加中国遗传学会表观遗传学分会和中国细胞生物学学会染色质生物学分会联合主办，武汉大学承办的"2023表观遗传与染色质生物学大会"。8月14日报道，18日离会，持续5天。

总体来说收货还是很大的，听老师们分享了不少很精彩的工作，无论是生物学规律的发现、技术工具的开发、计算框架的搭建等都有不错的涉及。很多talk跟我们的方向并不那么契合，但是听听总能有些收货。

5天的talk，接近70位老师分享了自己的工作，各有千秋。受限于我自己的专业方向，对分子、生化的研究确实很不了解，很多研究表观遗传调控的分子机制的工作其实没太听明白，就只能浅浅记录几个对我而言比较impressive的工作。

## 1. 关于生物学问题


### 薛愿超：非编码RNA与转录调控
这个标题起得很大，但其实分享的主要就是薛老师上个月刚发表的Nature论文，通过系统的RIC-Seq研究RNA-RNA互作，并发现Alu元件在介导promoter-enhancer的选择性结合过程中发挥了重要作用，填补了之前对EPI特异性来源的空白。不得不说这真的是非常精彩的工作，生物学意义很强，而且无论是从数据分析还是后续生物学验证都做的很完整干净，证据扎实，确实让人眼前一亮……。这篇文章刚发表的时候，淑悦就在组会上系统分享了这个工作，淑悦讲的很清楚，汤老师对这个工作评价也极高，甚至建议大家在组会后都自己再看一遍论文原文，这是少见的。

![IMG_5653](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20230819/Nature_Alu.jpg)

薛老师是付向东老师的学生，付向东老师回国不久，这次也在speaker之列。值得一提的是，付老师在后来自己的talk中提到了关于EPI选择性的问题，还特意强调“这个问题前段时间薛愿超他们给了一个很不错的解决”，这大概就是“我的好学生”系列吧哈哈哈。

### 颉伟：Decoding the transcription circuitry when life begins
颉老师给的标题也很大，大概是因为他们做的工作覆盖ZGA调控的方方面面吧。不过他这次分享的也主要是一个故事，也是7月份刚刚发表在Nature上的研究（刚看了下文章状态是accelated review…这就是大佬的力量吗），关于OBOX家族的不同蛋白如何调控ZGA过程的子代基因激活。也是非常系统且完整的工作，从鉴定到OBOX蛋白家族，到统一家族不同蛋白的序列分析，单独敲除与rescue实验，再到同家族蛋白domain之间交换，鉴定到关键作用的蛋白domain，以及与Pol II相互作用，激活转录的机制，层层递进。从问题的提出，到一步步解决，每一步过程都有独立的实验验证，技术运用完美服务问题解决…赏心悦目。

![IMG_5653](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20230819/obox.jpg)

值得一提的是，提问环节同学问道颉老师怎么注意到OBOX家族，颉老师说这几个蛋白都是合子中翻译强度最高的几个蛋白，你看到data就不可能miss掉。确实，展示的结果中OBOX家族的几个蛋白翻译强度远远高于合子中所有其他蛋白，然到现在才被鉴定到，也得益于颉老师他们自己发展的低起始量的Ribo-Seq技术。我们也做了很多新技术，那我们怎么去做这样类似的生物学发现呢？


## 2. 关于新技术

### 李祥：Chemical approaches to decoding histone epigenetics
李祥老师是与会老师中为数不多的化学背景的科学家，分享了他们利用化学手段鉴定组蛋白修饰相关蛋白的新技术CLASPI (cross-linking-assisted and SILAC-based protein identification)。不同于生化实验中常用的pull down等方法，CLASPI直接用原位cross-link的手段结合荧光标记，可以非常高效地鉴定细胞中的表观修饰结合蛋白。一张印象深刻的slide是李老师着重强调，他们在一次CLASPI实验中就成功鉴定到了之前几乎所有报道过的H3K3me3的reader蛋白，这可是之前好几年的生化实验才给出的结果。更夸张的是通过进一步改进荧光标记策略，可以直接鉴定结合蛋白上起到识别与结合作用的蛋白domain，而且与结构生物学给出的结果非常吻合，甚至还可以标记结构无法解析的IDR区域…这就比较夸张了。而且化学方法的优势是很容易可以拓展到其他组蛋白修饰、DNA修饰甚至是RNA修饰，都有不错的表现（给生物学家们一点小小的chemical震撼hhh）。讲完茶歇时候李祥老师周围挤满了人，都要加老师微信哈哈哈，大家都看到了这些技术的巨大潜能。

### 骆观正：基于新测序技术的表观转录组解析
骆老师分享了两个技术，第一个是构建了一个完全modification-free RNA library，可以作为各种RNA修饰测序技术的负对照，以消除RNA二级结构、序列等非修饰因素对修饰检测的影响。这种阴性对照系统直接能发Nature Methods也反映了它确实很重要吧。另一个我更感兴趣的工作是他们开发了利用Nanopore Naive RNA Sequencing直接在单分子水平上检测RNA修饰的新技术，还是很fancy的。

## 3. 一些收获
### 关于技术与生物学问题的关系
这其实我一直在思考的问题，我是生物科学本科出身，当初科研的ambition也是做出一些关于人类疾病的生物学发现or治疗的线索。当初选择了生物信息学、基因组学作为自己的主要方向，也还是有一些关于生物学本身的关怀在。然而现在我主要做的研究方向很偏技术，主要还是做新一代测序技术的开发与应用，开发技术为主，所做的生物学是基于技术进步的，为技术背书的，说到底“生物学”的属性并不强。

我记得本科刚接触基因组学的时候和高歌老师聊天，高歌老师提到了多组学大数据时代下“data-driven”的研究与传统“question-driven”的生物学研究的本质区别，并嘱咐我们本科时候一定要上好数学、统计学的基础课程，以及分子生化等生物学课程，打好基础。后来待的实验室，无论是徐老师还是汤老师，都是以高通量测序为基础的数据驱动的研究：开题的时候只需要样本体系+技术就能源源不断产出数据，体系可以是发育可以是癌，技术可以是RNA-Seq可以是各种表观遗传测序，可以是bulk也可以是单细胞。虽然多组学大数据提供了强大的profiling能力，但如何从其中找到线索讲好故事其实是一个很困难的问题，这需要对所研究的生物学体系具有很深的认识，同时也对计算方法的理解与结果解读有很高的要求。很多时候拿到数据其实是无从下手，只能去看看别人分析类似的数据有什么套路。这也是我自己在科研过程中很struggle的地方：相比于做实验遇到一个一个阴性结果，完全不知道从哪里开始入手反而更加折磨。

这次给talk的老师里也有不少把多组学测序作为主要研究手段，给出非常好的生物学发现的，比如上面提到的颉伟老师和薛愿超老师。两位老师都是发展新的测序技术同时研究新的生物学问题，但仔细想想也不难发现二者其实还是存在一些差别的。薛愿超老师分享的研究其实主要还是技术驱动、数据驱动的模式：薛老师2020年发表了RIC-Seq技术，可以系统研究RNA-RNA的相互作用。拿到新技术很自然就是想这个技术能有什么应用，基于此薛老师想到可以研究enhancer RNA和promoter RNA的相互作用，并用RIC-Seq对6个细胞系做了系统profiling，在对鉴定到的EPI中发现了promoter和enhancer上倾向于富集共有的Alu序列，只有又通过敲除、敲入等等一系列实验验证Alu在这个过程中的作用，属于是从技术到数据、再从数据到生物学发现、最后通过实验验证生物学发现。颉伟老师则不一样，因为他们实验室有非常明确的生物学问题，就是ZGA过程中合子基因表达启动的调控机理，而且在这个问题上做出了很多优秀的生物学发现。他们是为了研究这个过程，自然地想到要去研究ZGA之前合子中主要翻译产生的蛋白质可能对ZGA过程有重要作用，因此开发了少量细胞的Ribo-Seq去测翻译组，发现了OBOX这一个蛋白家族的转录因子，并做了系统的功能实验和蛋白结构域功能分析。两位老师思路不同，但讲的都是逻辑清晰、完整而系统、且生物学意义重大的发现。

结合自己的科研来看，其实我们现在处在一个很尴尬的中间位置：我们既没有强大的资源和数据分析能力去做超大规模的atlas resource，没有成熟的经验体系去结合大量公开数据集做一些大数据驱动的计算模型，也没有系统而成熟的生物学体系与生物学问题。我们开发新技术，然后利用新的技术去解决之前不能解决的问题，做的工作很多时候还是新的维度的profiling。我前几年都在做新一代测序技术的开发，虽然新技术开发确实是难度比较大的课题，需要处理很多之前没有遇到过的问题，但其实也有好处就是很多东西是有成熟的评价标准的。拿SCAN-Seq2举例，这种单细胞RNA-Seq的技术从灵敏度、交叉污染、重复性、定量准确性等等等各个指标都有成熟的评价方法、有如ERCC这种可用的内参体系，所以需要解决的就是关于技术本身的问题，费功夫但不费脑子。最近一两年开始做真正生物学意义的课题，主要focus在癌症上，才真正意识到在面对具体的生物学体系时候，如何从profiling的data中找到生物学故事的线索，提出问题并解决问题，这才是真正困难的部分。这需要大量的文献阅读和对这一领域过去、现状和未来研究方向的理解与思考，否则纵使掌握了再多组学数据分析的奇技淫巧也无处发力。最近也做了一些积极的尝试，从癌症的分子压型入手、先重复出已经报导并广为接受的压型种类，然后结合单细胞技术和表观遗传技术的优势去找新的生物学切入点，再对找到的高置信度target做实验验证。套路上看起来确实有模有样，但仍感觉在data mining这方面仍然有巨大的进步空间。

### 关于presentation的重要性
这次开会一个很重要的收获，也是和同行几位同学狠狠共鸣的点，是真切感受到了“讲好一个报告”的能力真的非常重要，甚至不亚于“做好一个研究”。很多老师做了非常漂亮的工作，但报告presentation讲得并不尽人意，或是PPT内容太多语速太快、什么都想讲但其实大家根本follow不上，或是内容衔接毫无逻辑性，只是简单的结果展示和PPT reader。相反的，有很多老师则不仅做了很漂亮的工作，还用一种非常精彩的方式讲了出来，从问题的发现到一步一步推进，层层深入，逻辑严密，简洁明了。这里非常值得一提的是中国海洋大学的高珊老师，讲的是以四膜虫为模式生物研究DNA上6mA修饰的遗传方式解析，给了一个非常好的如何讲报告的范式。甚至在提问环节，场下的付向东老师还专门走到话筒前说“我不提问题，我就是给一个comments：非常漂亮的报告，真正做到的show的都讲，不讲的不show，希望大家可以学习”。“how的都讲，不讲的不show”这是我第一次听到这个提法，但想想我自己确实有时候受限于时间会没法address自己PPT上的每一个点。想起来之前李毓龙老师也说过，准备presentation最难的不是做加法，而是做减法，如何在给你的时间内选择合适的结果把你的故事讲清楚，这是一个很重要的问题。

## 总结

这次去开会最大的感受是出去开会真的很累……完全不是一开始想想的快乐摸鱼。前两天每天早上8点50开始讲座，一直讲到晚上快10点，中间就只有两顿饭的休息时间，到晚上整个脑子都不转了。后两天安排稍微轻松一点，就去武汉市内到处走了走，高温预警+超大湿度下一下午两万步，直接人都累麻了，腰也疼得不行，回来周末直接寝室躺两天才缓过来。

回来继续自己的科研，还是希望能做出点有意思的生物学发现吧，不要做完测序就发现自己只会做测序了……


  <p align="right">振宇</p>

  <p align="right">于畅春新园</p>

  <p align="right">2023年8月19日</p>
