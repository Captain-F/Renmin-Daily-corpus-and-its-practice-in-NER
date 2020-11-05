# 人民日报语料库及其在NER任务的使用
 
 ***仅用于交流和练习***  

## 人民日报语料库 (1998.1)
### <本库存在的意义>
  * 主要在于能够直接提供用于NER任务的处理好的语料, 分别是基于词级和字级任务的NER数据。
### 识别的实体及标注
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
  * 模型的代码过几天再更，最近事情较多.......
* BERT + BiLSTM + CRF (character-level) 
* word + character
