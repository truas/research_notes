### Multi-Task Deep Neural Networks for Natural Language Understanding

---
- [Zotero Select Link](zotero://select/groups/2480461/items/HAIA27PX)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/HAIA27PX)
- Author: [[Xiaodong Liu]] [[Jianfeng Gao]]
- Topics: [[multi_task_learning]] [[language_models]]
- Venue: #arXiv 
- Year: #2019
---
### Techniques
- Apply four heads for 9 different [[GLUE]] tasks on a transformer encoder (e.g., single-sentence classification, pairwise text similarity, pairwise text classification, and pairwise ranking) and train by updating one batch per task in each training step.

![[2019_Multi_Task_DNN_for_NLU.png]]

---
### Goal
- To create a Multi-Task model for learning representations across multiple NLU tasks.
---


### Major Contributions
- Train one model on multiple tasks to perform each of those tasks with high accuracy
---

### Secondary Contribution
- Higher performance for other data sets with fewer examples than [[BERT]]. High generalization through multiple tasks which leads to higher peformance on new datasets.
---

### Limitations/Future Work
- Deeper understanding of model structure sharing in multi task learning
- A more effective training method that leverages relatedness among multiple tasks, for both fine-tuning and pre-training [[UniLM]].
---

### Notes (Try to use backlinks)
---
