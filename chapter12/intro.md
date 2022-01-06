# 第十二章 句法成分（*Constituency Grammars*）

对语法的研究很早就开始了。梵语的语法是由印度语法学家 Pāṇini 在公元前 7-4 世纪之间的某个时候，在他著名的论文 Aṣṭādhyāyī（“8 books”）中描述的。而我们的词 **syntax** 来自希腊语 *sýntaxis*，意思是“排列在一起或安排”，指的是词语排列的方式。我们在前几章已经看到了各种句法概念：词语序列的排序（第 2 章），这些词序列的概率（第 3 章），以及使用词性作为词的语法等价类（第 8 章）。在这一章和接下来的三章中，我们将介绍各种句法现象，这些现象远远超出了这些简单的方法，以及用计算方式（*computationally useful manner*）来获取它们的形式模型（*formal models*）。

本章的大部分内容是关于上下文无关文法（*context-free grammar*）的。上下文无关文法是许多自然语言（以及计算机语言）句法（*syntax*）的形式模型的骨干。因此，它们在许多计算应用都有发挥作用，包括语法检查、语义解释、对话理解和机器翻译。它们非常强大，可以表达句子中词语之间的复杂关系，而且在计算上又是易处理的，所以也存在用它们来解析句子的有效算法（正如我们在第 13 章中所展示的）。在第 16 章中，我们展示了它们如何为语义解释任务提供一个系统的框架。在这里，我们还介绍了词法化文法（*lexicalized grammars*）的概念，重点聚焦在一个例子，即**组合范畴语法**（*combinatory categorial grammar*），或称 **CCG**。

> 译者注：语法和文法均指 *grammar*，具体如何翻译主要参照主流译法。

在第 14 章中，我们将介绍一种称为**句法依存**（*syntactic dependencies*）的语法形式模型，它是这些成分语法的替代物，我们也将给出**依存分析**（*dependency parsing*）的算法。成分和依赖的形式化对语言处理都很重要。

最后，我们以 ATIS（Air Traffic Information System）(Hemphill et al., 1990)[^1] 为例，给出一个英语语法的简要概述。ATIS 系统是一个早期的口语系统，用于用户通过类似 *I'd like to fly to Atlanta* 的简单句子预订航班。

[^1]: Hemphill, C. T., J. Godfrey, and G. Doddington. 1990. The ATIS spoken language systems pilot corpus. Proceedings DARPA Speech and Natural Language Workshop.
