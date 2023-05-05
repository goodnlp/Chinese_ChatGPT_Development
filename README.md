# Chinese_ChatGPT_Development
## 目录
* 引言
* 数据的准备
* 模型编写和训练
* 研发过程中的收获，总结和反思

## 引言
ChatGPT已经引发信息时代的又一轮革命，但是中文世界的模型发展却很滞后，本项目主要目的是在中文ChatGPT模型的研发做一些探索，这个项目也只是用于教学或者研究目的，由于计算资源和人力有限，并不能用于生产上线服务。<br />
机器学习的研发包含三个基本要素，数据，模型，算力，本项目着重于前两个因素。

## 数据的准备

(1) 预训练语料
* 维基百科中文词条的所有数据（2019版），文件大小518.7M, 链接: https://pan.baidu.com/s/1eCE_Ez_fTA4AllkCds-x_Q?pwd=3242 提取码: 3242
* 百科问答数据集（2019版本），文件大小650M,  链接: https://pan.baidu.com/s/1odVtlPULLFZVNZmpk1m8rA 提取码: 9x2f

(2) 有监督训练数据集 <br />
有监督训练是指，给定一个特定的输入，模型应该学习到正确的输出。比如情感分析任务，输入“我今天很高兴”，那对应的输出应该是积极情感。这里其实就是训练instruction GPT的过程了。

* 分类任务数据集
    * 头条数据集，链接: https://pan.baidu.com/s/1aSB6uYxImuF-KYy7hkU_qg 提取码: 86jr
    
(3) 多轮对话数据集
openai的chatGPT的一个明显能力是具有很强的感知上下文的能力，这就让交互更加流畅自然。这样的能力的获得肯定是要特定的数据来训练的，因此本项目也会囊括下面的数据集。
* 豆瓣多轮对话数据集，链接: https://pan.baidu.com/s/167CYM7vSIEoWGcND1w4lTQ 提取码: 6tiv

(4) 训练Reward model的数据集 <br />
这是需要人工标注的，就是上述模型针对一个输入，输出一个句子，人工需要对其打分，分数从1到5分布，人工需要判断，越符合人的需要，打分越高。<br />
这个数据集要多大呢，目前ChatGPT没有公布具体数字，只能先自行摸索了。<br />
当然，数据集数量大小是一方面，输入句子的种类分布均匀且具有代表性也很重要。<br />
由于这个项目的目的并不是“调教”出一个可以直接用于生产环境的模型，这个项目的目的在于把训练ChatGPT的过程走一遍，积累一些定性的经验，因此，最终标注的数据量不会多大。

## 模型编写和训练
(1) 预训练
* gpt预训练脚本在这里： https://github.com/goodnlp/Chinese_ChatGPT_Development/tree/main/code

* 已经训练好的模型文件在这里： 链接: https://pan.baidu.com/s/19K2RNXccn2JQS-T7tAZ7zw 提取码: 35ih

(2) finetuning （in progress） <br/>

这一步是指用现存的各类标注好的NLP数据集对finetune 预训练模型

* 代码
* 模型文件

(3) reinforcement learing with human feedback （in progress）

* human feedback是指人工对模型输出的回答进行打分（1-5）

* actor_critic model

* reward model


## 研发过程中的收获，总结和反思
* 多GPU训练是很重要的，多GPU的使用可以训练更大的模型；如果只支持多卡多机器训练那就更好了，可以快速训练模型
* 算法理论的理解是基础，但是工程实践在这个项目中更是chatGPT成功的关键，在搞出来之前，每一步都没有说必须得怎么做，要达到惊艳的效果，却是要熟稔方方面面，在此基础进行尝试。

