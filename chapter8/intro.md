# 第八章 用于词性和命名实体的序列标注（*Sequence Labeling for Parts of Speech and Named Entities*）

亚历山大的 Dionysius Thrax（约公元前 100 年），或者也许是其他人（这是一个漫长的过程），写了一篇希腊语语法草稿（一个“*technē*”），总结出了他当时的语言学知识。这部作品是许多现代语言学词汇的来源，包括 syntax、diphthong（*译者注：双元音*）、clitic（*译者注：附着语素*）和 analogy（*译者注：类比*）。还包括对 8 个**词性**（*parts of speech*）的说明：名词（*noun*）、动词（*verb*）、代词（*pronoun*）、介词（*preposition*）、副词（*adverb*）、连词（*conjunction*）、分词（*participle*）和冠词（*article*）。虽然早期的学者（包括亚里士多德以及斯多葛派）都有自己的词性列表，但在接下来的 2000 年里，正是 Thrax 的这一套八种词性成为了欧洲语言描述的基础。（甚至我们儿时的 *Schoolhouse Rock* 教育电视节目，其中都有关于这 8 个词性的歌曲，比如已故的伟大的 Bob Dorough 的 *Conjunction Junction*。）词性在两千年中持续发展，足以说明它们在人类语言模型中的核心地位。

专有名词（*Proper names*）是另一个重要且古老的语言学类别。虽然词性通常是分配给单个单词或语素，但专有名词通常是整个多词短语，例如人名“Marie Curie”、地点“New York City”或组织“Stanford University”。粗略地说，我们将使用**命名实体**（*named entity*）一词来表示任何可以用专有名词指代的事物：一个人，一个地点，一个组织，尽管我们将看到这个术语通常被扩展到那些本身不是实体的事物。

词性（又称 **POS**）和命名实体是了解句子结构和意义的有用线索。知道一个词是名词还是动词，就可以知道其可能的相邻词（英语中的名词前面是限定词（*determiners*）和形容词，动词后跟着名词）和句法结构（动词与名词有依存关系），这使得词性标注称为解析的一个关键方面。知道一个命名实体是一个人名、一个地名还是一所大学，这对许多自然语言理解任务（如问题回答、立场检测（*stance detection*）或信息提取）都非常重要。

在本章中，我们将介绍**词性标注**（*part-of-speech tagging*）的任务，即给定一个词的序列，给每个词分配一个词性，如 NOUN或 VERB，以及**命名实体识别**（*named entity recognition*）（NER）的任务，给词或短语分配标签，如 PERSON、LOCATION 或 ORGANIZATION。

在这些任务中，我们为输入词序列中的每个词 $x_i$ 分配一个标签 $y_i$，从而使输出序列 $Y$ 与输入序列 $X$ 具有相同长度，这被称为**序列标注**（*sequence labeling*）任务。我们将介绍经典的序列标注算法，一种是生成式的 —— 隐马尔可夫模型（*Hidden Markov Model*）（HMM），另一种是判别式的 —— 条件随机场（*Conditional Random Field*）（CRF）。在接下来的章节中，我们将介绍基于 RNN 和 Transformer 的现代序列标注方法。
