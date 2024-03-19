### DistilBERT, a distilled version of BERT: smaller, faster, cheaper and lighter
---
- [Zotero Select Link](zotero://select/groups/2480461/items/KZXBZ24C)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/KZXBZ24C)
- Authors: [[Victor Sanh]] [[Thomas Wolf]]
- Topics: [[nlp_ann]] [[nlp_distill]]  [[nlp_embeddings]] [[nlp_lm]] [[nlp_task]] [[nlp_transformers]]
- Venue: #arXiv
- Year: #2020
---
### Techniques
-[[_2018_BERT]]
	- Triple loss combining language modeling (¯\_(ツ)_/¯):
		- removing [[MLM]]
		- 
	- [[nlp_distill]]
	- cosine-distance loss 

---
### Major Contributions
- Distilled version of [[_2018_BERT]]:
	- 40% of its size
	- 60% faster
	- 97% of its language understanding capabilities
- Knowledge distillation. Student/Teacher training model
	- Bucila - Model compression 2006
	- Hinton - Distilling the knowledge in a neural network 2015 #TODO
		- [[softmax-temperature]]
- They dropped [[NSP]]
- Very large batches (up to 4K) + dynamic masking
---
### Secondary Contribution
- Linear and last variations on the last dimension of the tensor showed small impact on computation efficiency (for a fixed parameters budget) than variations on other factors like the number of layers. 
- Right initialization for the sub-network to converge helps
- It is beneficial to use a general-purpose pre-training distillation rather than a task-specific distillation
- Leveraging the teacher’s knowledge with initialization and additional losses leads to substantial gains.
- Recent developments in weights pruning reveal that it is possible to remove some heads in the self-attention at test time without significantly degrading the performance Michel 2019 - Are sixteen heads better than one? #TODO
---
### Limitations/Future Work
- Should [[NSP]] be wipped out completely or another alternative task should be incorporated?
---
### Notes (Try to use backlinks)
- Some references for [[nlp_cost]] and environmental concerns over large models
- Tasks: #SQuAD #GLUE 
- Available at #hugging-face 
---
