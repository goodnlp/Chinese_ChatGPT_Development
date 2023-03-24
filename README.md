# Chinese_ChatGPT_Development
## 目录
* 引言
* 数据的准备
* 模型编写和训练
* 研发过程中的收获，总结和反思

## 引言
ChatGPT已经引发信息时代的又一轮革命，但是中文世界的模型发展却很滞后，本项目主要目的是在中文ChatGPT模型的研发做一些探索，这个项目也只是用于教学或者研究目的，由于计算资源和人力有限，并不能用于生产上线服务。

## 数据的准备

(1) 预训练语料
* 维基百科中文词条的所有数据（2019版），文件大小518.7M, 链接: https://pan.baidu.com/s/1eCE_Ez_fTA4AllkCds-x_Q?pwd=3242 提取码: 3242
* 百科问答数据集（2019版本），文件大小650M,  链接: https://pan.baidu.com/s/1ZB-rX3bj0xtrp1t_yA2Xmw?pwd=2023 提取码: 2023

(2) 有监督训练数据集\n
有监督训练是指，给定一个特定的输入，模型应该学习到正确的输出。比如情感分析任务，输入“我今天很高兴”，那对应的输出应该是积极情感。这里其实就是训练instruction GPT的过程了。

* 分类任务数据集
    * 头条数据集，链接: https://pan.baidu.com/s/1jHnUpF_F94Z1f-IWFmWvDA?pwd=vdt4 提取码: vdt4 



## 模型编写和训练


## 研发过程中的收获，总结和反思
