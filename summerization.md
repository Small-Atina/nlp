https://www.jiqizhixin.com/articles/2019-03-25-7
https://mp.weixin.qq.com/s/Aye9FBwG-v2JO2MLoEjo0g
### 自动生成摘要分类
#### 有监督和无监督
#### 抽取式和生成式
#### 单文档和多文档
### 抽取式摘要
**从source中选择合适的句子作为summeries，要求被选择的句子有两个特性：1.包含source中全部重要信息，并在逻辑上保持一致；2.具备最低的冗余性，即包含类似的信息的句子不应同事出现**
**抽取式摘要实际上可以当做是一个每个句子进行一个二分类的问题，但是会出现文本上连贯性不尽人意，还可能会出现代指实体，需要对其进行指代消解**
#### 可以根据预训练模型出现的时间分为两个阶段
##### 2015--2018 RNN-based Summerise
##### 2019-2020 Transformer-based Summerise
+ TextRank
+ Lead
+ BertSum
### 生成式摘要
**根据source的重要信息，由decoder自发的生成summerise。同样也满足信息性和冗余性**
****
+ seq2seq+attention
+ PGN+Coverage
#### 关系哪个nlp的哪个领域，有什么进展？
