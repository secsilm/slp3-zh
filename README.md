# Speech and Language Processing 3rd Edition 中文翻译

《自然语言处理综论》第三版翻译。原文：[Speech and Language Processing](https://web.stanford.edu/~jurafsky/slp3/)。

若无特别说明，文中括号或者引用块中的 *斜体字* 为对应的英文原文或者我自己注释的话（会标明 *译者注*），引用块开头若标明「译者注」，则整个引用块都是我自己注释的话。否则为原文中本来就有的话。

## 在线阅读

本翻译系列目前可以在以下平台在线阅读：

- 【推荐】知乎。链接：[自然语言处理综论第三版中文翻译系列导读 - 知乎](https://zhuanlan.zhihu.com/p/365853153)。注意不是实时发布，会在翻译完整节之后同步到知乎。对脚注和数学公式等格式支持较好。
- GitBook。链接：[Introduction - slp3-zh](https://secsilm.gitbook.io/slp3-zh/)。与 GitHub 保持实时更新。不支持脚注，会被直接吃掉。由于行内公式使用的是 `$$`，所以行内公式无法正常显示。
- GitHub。链接：[secsilm/slp3-zh: 《自然语言处理综论》第三版翻译。](https://github.com/secsilm/slp3-zh)。内容最新。不支持脚注，但不会被吃掉。数学公式完全不支持。

## 进度

- 第二章 正则表达式，文本规范化，编辑距离
  - [Intro](chapter2/intro.md)
  - [2.1 正则表达式](chapter2/2.1_Regular-Expressions.md)
    - 2.1.1 基础正则表达式模式
    - 2.1.2 逻辑或，组合和优先级
    - 2.1.3 一个简单的例子
    - 2.1.4 更多的运算符
    - 2.1.5 一个更复杂的例子
    - 2.1.6 替换，捕获组（*Capture Groups*）和 ELIZA
    - 2.1.7 先行断言
  - [2.2 词](chapter2/2.2_Words.md)
  - [2.3 语料库](chapter2/2.3_Corpora.md)
  - [2.4 文本规范化](chapter2/2.4_Text-Normalization.md)
    - 2.4.1 用于粗略分词和规范化的 Unix 工具
    - 2.4.2 分词
    - 2.4.3 用于分词的字节对编码
    - 2.4.4 词规范化，词形还原和词干提取
    - 2.4.5 分句
  - [2.5 最小编辑距离](chapter2/2.5_Minimum-Edit-Distance.md)
    - 2.5.1 最小编辑距离算法
  - [2.6 总结](chapter2/2.6_Summary.md)
- 第八章 用于词性和命名实体的序列标注
  - [Intro](chapter8/intro.md)
  - [8.1 英语词类](chapter8/8.1_(Mostly)-English-Word-Classes.md)（*进行中*）

## TODO

接下来计划要翻译的章节：

- [ ] 【进行中】[Chapter 8: Sequence Labeling for Parts of Speech and Named Entities](https://web.stanford.edu/~jurafsky/slp3/8.pdf)（27 页，[2.5.1](chapter2/2.5_Minimum-Edit-Distance.md) 中提到）
- [ ] [Chapter 12: Constituency Grammars](https://web.stanford.edu/~jurafsky/slp3/12.pdf)（30 页）
- [ ] [Chapter 13: Constituency Parsing](https://web.stanford.edu/~jurafsky/slp3/13.pdf)（22 页，[2.5.1](chapter2/2.5_Minimum-Edit-Distance.md) 中提到）
