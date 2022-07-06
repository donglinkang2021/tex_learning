# `tex`写作开启

[TOC]

## `CTec+miktex+texstudio`

> 这个主要参考的是这个博客[(140条消息) LaTeX相关概念介绍及CTeX、MiKTeX+TeXstudio环境搭建_viacm的博客-CSDN博客_miktex就是latex吗](https://blog.csdn.net/qq_37556330/article/details/106119151)
>
> ，实测运行效果不错，但还是想说一下自己的使用感受。

### `texstudio`

- 本来想从sourceforge下载，奈何太慢，就又重新从[Releases · texstudio-org/texstudio (github.com)](https://github.com/texstudio-org/texstudio/releases)这里去下了现在使用的版本，总体上使用比较顺心，网上一大堆博客说它的好，其中大概印象深刻有几点：
  - 插入表格和图片相对简单；
  - 左边代码右边预览的方式很香；
  - 一键编译运行减少操作次数，nice;

### `CTeX+MiKTeX`

- 请注意，博客里说的是先装`CTeX`再装`MiKTeX`到相应`CTEX`文件夹内去，由于本人总是没有细看文档乱搞，导致在路径这方面犯了很多错误，配置的环境变量往往都不对；
- 其实只装`MiKTeX`也已经满足基本使用了，使用方法：
  - 安装完成后有两个文件：`TeXworks`和`MiKTeX consoles`
  - 前者用于直接写代码编译运行产生pdf
  - 后者用于安装缺的宏（`packages`）
  - 如果是从`CTAN`上下载安装的话，通常下载的都是压缩包，解压后把对应文件夹拉到，`miktex\tex\latex`的目录下即可，记得要要把`.ins`文件编译成`.sty`文件，方法，cmd输入`latex <packages.ins>`例如`latex datetime.ins`

### 评价

`CTeX`是支持中文的`Tex`，但里面的`MiKTeX`过于老旧了所以要用下载一个额外的扔里面，但其实也可以去清华大学那个网站下载[Index of /ctex/legacy/2.9/ | 清华大学开源软件镜像站 | Tsinghua Open Source Mirror](https://mirrors.tuna.tsinghua.edu.cn/ctex/legacy/2.9/)`_Full.exe`后缀的文件，这样会好一点点，但本人用的不是这个其实也okay；但当从要不断地去网上找包来下的这一点的话，对于网络不好的人其实不太友好——这时宁愿笨重的一次性解决可能才是王道:rose:——
$$
{\large \mathcal{Tex\;live}} \;\&\&\; {\color[RGB]{255,0,255} {\huge \mathbb{tex\;studio}}}   +template+latexlive=\\{\Huge \mathfrak{Elegant}   }
$$
[在线LaTeX公式编辑器-编辑器 (latexlive.com)](https://www.latexlive.com/)





## `Texlive+TeX studio`最香的`tex`排版方式

- 安装参考这个博客：[(140条消息) LaTeX学习：Texlive 2019和TeX studio的安装及使用_Mikchy的博客-CSDN博客_texlive2019](https://blog.csdn.net/Mikchy/article/details/94448707)

上面这个博客包含了一些基本的配置还有一个论文引用管理的扩展什么的，觉得博客里有句话说的很对，与其不停的查缺哪个包再去安装编译，我们不如把精力专注于写作上面还有知识的积累和储备；

> `LaTeX`主要的就是利用模板，所以一般如果写论文的，导师或者投稿的那里都会有模板拿来使用的，因此最主要的就是
>
> 知道如何编写**数学公式**

- 基本使用可以参考的是这个博客：[(140条消息) TexStudio的安装及简单使用（持续更新）_Vgdog的博客-CSDN博客_texstudio](https://blog.csdn.net/dogfat/article/details/106962966)

这个博客的最后还附上了IEEE论文模板的地址[Create Your IEEE Journal Article - IEEE Author Center Journals](https://journals.ieeeauthorcenter.ieee.org/create-your-ieee-journal-article/)，在这个文件夹中下载了一个会议的模板，可以酌情学习其中的排版方式，由于现在暂时没有写这种专业论文的需要暂且把资源放在这里；

![image-20220706211220851](https://img2022.cnblogs.com/blog/2737817/202207/2737817-20220706211427900-190038002.png)

## 感受:cry:

在接触`tex`之前一直都是单纯用`latex`写一些简单的数学公式就好，没有想过要去配那些各种奇奇怪怪的包或者装一个专业的`tex studio`，一开始有其他学校的朋友说他们老师建议使用的是`MiKTeX+Sublime Text+Sumatra PDF+Texmaker`，自己也试着使用了一下，前面几个自己都一一配置好了，最后在`Texmaker`上调配置上老调不对，它需要的`MiKTeX`的版本远比自己下载的要旧的多，于是最后改用了：`CTeX+MikTeX+Texstudio`用`CTeX`主要还是因为它支持中文，但后面又发现把其他人博客的代码粘过来的时候运行，总是会提示缺这个缺那个包，最后的最后才是用了现在的方案，`Texlive+TeX studio`，只能说相比之前两种方式可以说是最省心的排版操作了，最后还找到一本书：

> 《`LaTeX入门`》刘海洋著

看了一下，再对比一下之前看到的博客质量，自己又有了新的体会（要是能早点知道有这本书也不至于自己东滚西爬遇到这么多问题了）

> 网上遇到的博客质量确实良莠不齐，靠遇到一篇真正用心写出来的文章来解决问题的效率全由运气决定——但如果有了扎实的基础知识可能就完全不一样了，我们会容易看出哪些博客是真正大佬写的（符合我们需求的），另外一些是小白在碰壁的过程中写的，不可否让，二者都对当下问题的解决会起到作用，但从长远目光，可能我们需要的更多是大佬的文章，减少信息差，才能少走弯路——当然弯路真的让人收获挺多的——有时白白坐在座位上瞎想，根本没意识到大佬在讲压箱底的经验，那还是建议自己去多走弯路多碰壁吧！
>
> ---个人摸索入门与读书感受:thinking:
