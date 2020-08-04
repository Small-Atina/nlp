#### 文本生成任务（翻译，对话，摘要）（baseline  seq2seq+attention）
+ 存在的问题
> 1. eq2seq模型是无法解决输出序列的词汇表会随着输入序列长度的改变而改变的问题。
> 2. oov的问题
+ 提出PtrNet 这类网络来解决这些问题。PtrNet主要应用于NLP的文本摘要任务、对话任务、（特定条件下）的翻译任务，目的在于应对OOV问题。
#### 一、Pointer Networks（发表于2015年）
##### 1.可以用Pionter Network解决的问题或者场景
+ 目标序列的词表，和源序列的词语内容是强相关的。面对不同语言、不同应用场景的任务，往往需要重新构造词表。
+ 词表的长度需要在模型构建之前作为超参数进行配置。如果需要变更词表的长度，就需要重新训练模型。
+ 在部分任务场景里，不允许有OOV的存在。
##### 2.Pionter Network主要思想,创新点。
> decoder的时候用对齐系数a(也就是attention)，得到其中值最大的那个维度作为指针。
> decoder输出一个由目标序列指向源序列的指针序列。
> 换句话说，传统带有注意力机制的seq2seq模型输出的是针对输出词汇表的一个概率分布，而Pointer Networks输出的则是针对输入文本序列的概率分布。
#### 二、CopyNet（发表于2016年）
##### 1.主要创新点
+ 有两个模块，Generate-Mode & Copy-Mode。Generate-Mode & Copy-Mode模块会维护两个词表，一个是传统的词表（但是这个词表不包含UNK），一个是源序列中的词构成的词表。
> 1. 对于传统词表中的词和UNK，模型采用Generate-Mode计算词语输出概率：
> 2. 对于源序列词表中的词，模型采用Copy-Mode计算词语输出概率：
> 3. 最后模型会将Generate-Mode和Copy-Mode输出的词语概率进行相加汇总，得到最终的词语概率分布。$p(w)=p(w|g)+p(w|c)$
+ state Update（重点）
#### 三、PGN(Pointer Generater Network)（发表于2017年）
##### 1.创新点
+ Generater Network
+ 
+ Coverage Mechanism
##### 2.CopyNet和PGN的区别是什么
+ 虽然都是用了generater和copy
