## 利用ALBERT+LSTM模型实现序列标注算法

### 数据集

1. 人民日报语料集，实体为人名、地名、组织机构名，数据集位于data/example.*;

2. 笔者自己标注的时间数据集，实体为事件，数据集位于data/time.*

### 模型

&emsp;&emsp;模型结构图如下：

![](https://github.com/percent4/ALBERT_BER_KERAS/blob/master/albert_bi_lstm.png)

&emsp;&emsp;训练效果如下图：

![](https://github.com/percent4/ALBERT_BER_KERAS/blob/master/example_loss_acc.png)

### 预测

```
Please enter an sentence: 昨天进行的女单半决赛中，陈梦4-2击败了队友王曼昱，伊藤美诚则以4-0横扫了中国选手丁宁。
{'LOC': ['中国'], 'PER': ['陈梦', '王曼昱', '伊藤美诚', '丁宁']}
Please enter an sentence: 报道还提到，德国卫生部长延斯·施潘在会上也表示，如果不能率先开发出且使用疫苗，那么60%至70%的人可能会被感染新冠病毒。
{'ORG': ['德国卫生部'], 'PER': ['延斯·施潘']}
Please enter an sentence: “隔离结束回来，发现公司不见了”，网上的段子，真发生在了昆山达鑫电子有限公司员工身上。
{'ORG': ['昆山达鑫电子有限公司']}
Please enter an sentence: 真人版的《花木兰》由新西兰导演妮基·卡罗执导，由刘亦菲、甄子丹、郑佩佩、巩俐、李连杰等加盟，几乎是全亚洲整容。
{'LOC': ['新西兰', '亚洲'], 'PER': ['妮基·卡罗', '刘亦菲', '甄子丹', '郑佩佩', '巩俐', '李连杰']}
```