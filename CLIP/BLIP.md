# 论文名称  BLIP: Bootstrapping Language-Image Pre-training for Unified Vision-Language Understanding and Generation
  [[BLIP.pdf]]
## 一句话  
  
自动清洗数据集
报告生成
  
## 属于什么方向  
  
Generation CLIP    
## 它解决的问题  
  
数据集中有噪声
模型不能生成
  
## 核心Idea
  
1.CapFilt：自己先生成关于图片的文字（Captioner），与原文字和图片分别进行相似度打分（Filter：把两组图文对送进ITC（图文匹配打分）），取高分者为训练集的文字--自动数据清洗！！
2.MED：编码器解码器同时拥有。
3.训练三个损失函数，ITC（相似向量空间距离拉近（CLIP）），ITM（判断图文是否是一对），LM（自回归预测下一个词），且共用参数
  
## 为什么想到这个Idea  
  
大家只想到了扩大数据，为什么不认真对待已有数据，做清洗？  
  
## 我学到了什么  
  
数据质量！自动清洗！

## 它没解决什么  
  
一句话  
  
## 我能继续做什么  
  
- 想法1  
- 想法2  
- 想法3  
  
## 相关论文  
  
[[BLIP-2]]