 # 论文名称  InstructBLIP: Towards General-purpose Vision-Language Models with Instruction Tuning
 
  [[InstructBLIP 1.pdf]]
## 定位  任务进入微调
  
#### 属于什么方向  

Instruction Tuning
#### 它解决的问题  

训练一个可以用于具有任务针对性的视觉模型  
## ※※作者思维链  
  
以前：  BLIP只喂给模型图像
缺陷：  在下游问答环节，不同任务没有不同的训练，全靠的一套Query
观察：  特定任务，Query的注意力应该有所不同
因此提出：  把任务描述也tokenize，送入训练

## 核心创新

- 创新点1：instruction tuning：在BLIP-2基础上，增加针对不同任务的微调

- 创新点2：


## 我学到了什么  
  
- 知识  
  
- 方法  灵感来自于LLM的Instruction tuning
  
- 实验设计  
  
## 我没搞懂什么  
  
- 问题1：Instruction tuning到底是啥---任务的tokenize
- 问题2：改编了BLIP-2的哪些地方---训练时，额外把任务的tokenize扔给Q-Former
- 问题3：
  
## 本文没解决什么，我能想到什么，可以挑什么刺
  
- 想法1  
- 想法2  
- 想法3  
  
## 相关论文  
  
[[GLoRIA]]  
[[MedCLIP]]  
[[BioMedCLIP]]