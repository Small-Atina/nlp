#### 1、常用的分词方法
##### 基于词典（字符串匹配）
+ 前向最大匹配
+ 逆向最大匹配
+ 双向最大匹配
##### 基于统计
+ 基于n元统计模型（使得语言模型概率最大的分词情况）（有词不存在的情况，采用平滑技术）
+ 
#### 2、文本表示的方法
##### 离散表示 
+ 1.One-hot表示
> 实现步骤：根据语料库创建词表，然后给每一个词一个index，那么一个词用一个长度为词表大小的向量表示并且只有一个位置为0
> one-hot 表示的特点：只有一个位置为1其余为0；文本表示是一个稀疏矩阵
> 缺点：无法衡量一个词语的重要性；不同词是相互正交的，不能表示词语之间的关系；
+ 2.BOW (bag of word): 词袋模型
> 词袋模型对文本进行编码（不是字或者词）
> 一个文本的长度是
+ 3.tf-idf：词频-逆文档频率
##### 分布式表示
+ 4.n-gram
+ 5.Co-Occurence Matrix：共现矩阵
+ 6.Word2Vec
https://my.oschina.net/u/4277346/blog/4462686
使用word2vec提前预训练比直接用深度网络训练的好处？
word2vec参数对参数的影响？？
+ 7.Glove
+ 8.Fasttext
+ 9.ELMO
