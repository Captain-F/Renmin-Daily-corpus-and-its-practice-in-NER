# 人民日报语料库及其在NER任务的使用
 
 ***仅用于交流和练习***  
___（最近事情比较多，等手上的东西做完代码会及时更新）___

## 人民日报语料库 (1998.1)
### <本库存在的意义>
  * 主要在于能够直接提供用于NER任务的处理好的语料, 分别是基于词级和字级任务的NER数据。
### 识别的实体及标注
* 语料基本情况
  * 以行为粒度切分得到的句子数量为： 19484
  * 句子长度最大为： 659
  * 句子平均长度为： 57.55666187641141
  * 句子长度（前20）： [659, 637, 629, 603, 596, 582, 515, 488, 480, 470, 459, 448, 444, 440, 436, 435, 431, 428, 426, 426]
* BIO标注

| 原标签 | 名称  | 实体标签 |
| :------------ |:---------------:|:-----:|
| nr      | 人名 | B-PER, I-PER |
| ns      | 地名        | B-LOC, I-LOC |
| nt | 机构团体        | B-ORG, I-ORG |

句子中非上述实体均标注为O

### NER应用 （Baseline model）
* word2vec + BiLSTM + CRF (word-level)  
  * 31/31 [==============================] - 2s 77ms/step
  * ###Test###, epoch: 10 | F1: 95.0353 | precision: 95.009 | recall: 0.9506
* BERT + BiLSTM + CRF (character-level) 
* word + character
