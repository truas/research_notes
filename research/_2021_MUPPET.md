### Muppet: Massive Multi-task Representations with Pre-Finetuning
---
- [Zotero Select Link](zotero://select/groups/2480461/items/WVG9CZQP)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/WVG9CZQP)
- Authors: [[Armen Aghajanyan]] [[Sonal Gupta]] 
- Topics: [[nlp_lm]] [[nlp_meeting_sum]]
- Venue: #arXix 
- Year: #2021
---
### Major Contributions
- pre-finetuning (a certain numberr of tasks (15)) consistently improves performance for pretrained discriminators (e.g. RoBERTa) and generation models (e.g. BART) on a wide range of tasks (sentence prediction, common sense reasoning, MRC, etc.),
---
### Secondary Contribution
- pre-finetuning can hurt performance when few tasks are used up until a critical point (usually above 15) after which performance improves linearly in the number of tasks.
- We show that the pre-finetuned models  consistently require less data for fine-tuning - this quite trivial
- R3F was pivotal in getting MUPPET to work for BART. All other fine-tuning and pre-finetuning was done using standard SGD.
---
### Limitations/Future Work
- It's is not clear if the "new" pre-finetuning is the actual pre-training/intermediate training.
---
### Notes (Try to use backlinks)
- Pre-finetuning involves a massive multi-task learning step (4.8 million total training examples) performed on around 50 classification, summarization, question answering, and common sense reasoning tasks.
	-  Standard multitask scheme can be unstable and often fail to learn high-quality representations
-  [[_2019_MT-DNN]] show that by leveraging multi task learning, we can further improve performance on several language benchmarks on top of traditional pre-training
-  [[_2019_T5]] shows that incorporating multi-task learning ontop of larger models does not improve upon the standardized pre-training / finetuning. Thus the effect of multi-task learning across different pre-training methods is not fully understood. (the findings in MUPPET refute T5)
-  The tasks are divided into 4 big groups: Classification, Summarization, MRC, and Commonsense
-  Two strategies to learn multi-task representations at scale: Accumulating Gradients Across Tasks (Heterogeneous Batches) and Leveraging Better Finetuning.
	-  **Accumulating Gradients Across Tasks** - Our model is trying to optimize not a single objective but several potentially competing objectives to create a unified representation across several tasks during model training
	-  **Better Finetuning** - Instead of starting from scratch, we initialize our model with representations learned from self-supervised pre-training in pre-finetuning.
-  For Summarization tasks we show that our pre-finetuned BART model outperforms all other summarization baselines. Both of these tables report over data-sets available during the pre finetuning stage
-  Furthermore, although dependent on the dataset, this critical point is roughly between 10 and 25 tasks. This suggests that previously observed MTL limitations were not fundamental and can instead be attributed to the lack of sufficient scale.
---
