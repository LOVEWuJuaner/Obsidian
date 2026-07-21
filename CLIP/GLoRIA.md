# 论文名称 GLoRIA: A Multimodal Global-Local Representation Learning Framework for Label-efficient Medical Image Recognition
[[GLoRIA（局部对齐）.pdf]]
## 一句话 
  
全局对齐和局部对齐同时训练
  
## 属于什么方向  
  
Medical CLIP  
data-enhanced CLIP  （其实在CLIP之前）
  
## 它解决的问题  
  
ConVIRT全局对齐太粗糙，既然要求细粒度，就让图像局部与单词对齐  
  
## 核心Idea  
  
要学习局部细粒度，用注意力机制，将局部与单词对齐（Global and Local）
  
## 为什么想到这个Idea  
  
病理只在局部，全局可能捕捉不到 （符合人类直觉，医生看报告，就是一个词对应一个局部区域）
  
## 我学到了什么  
  
1.充分挖掘数据集
2.先前做的太宽，我只做里面一个更细的(更细的监督信号)
3.局部对齐到底是怎么做到的？----Cross Attention：一个word 的embedding a与它的图像的196个patch embedding做cross attention得到向量aA，与一些其他图像的196个patch做cross atteneion得到aB，aC.....然后再用向量b，向量c，依次类此操作，得到矩阵
    a  b  c
aA
aB
aC

然后对矩阵做InfoNCE，（经过一些还没理解的原理），a就与最相关的patch变得相似。
## 它没解决什么  

1.Attention找的区域，未必是真正的病灶（Attention不可靠！）（重要！！后续大多数都是想解决这个问题）
2.报告的每个词都来attention 每个patch，是不是很多没用的句式，单词，徒增训练量？？---这也可能是MedKLIP的灵感启发，用三元组先结构化每个实体
  
## 我能继续做什么  
  
- 想法1  该如何定位病灶呢？结合现有大模型可以吗
- 想法2  
- 想法3  
  
## 相关论文  
  
[[ConVIRT]]  
[[MedCLIP]]  
[[BioMedCLIP]]