### Add title here
---
- [Zotero Select Link](zotero://select/groups/2480461/items/KLNL4BMW)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/KLNL4BMW)
- Authors: [[Xiao Liu]] [[Jie Tang]]
- Topics: [[nlp_transformers]] [[nlp_autoregressive]]
- Venue: #arXiv
- Year: #2021
---
### Major Contributions
- GPTs can be better than or comparable to similar-sized BERTs on NLU tasks with a novel method P-tuning which employs trainable continuous prompt embeddings.
- we propose a novel method– [[P-tuning]]– to automatically search prompts in the continuous space to bridge the gap between GPTs and NLU applications
- 
---
### Secondary Contribution
- We show that GPTs can be as competitive as BERTs in natural language understanding (sometimes even better) with P-tuning
- We show that P-tuning is a general method to improve GPTs and BERTs in both few-shot and fully supervised settings.
- 
---
### Limitations/Future Work
- P-tuning v.s. Fine-tuning. It is not allowed to change the pre-trained model’s parameters by fine-tuning in traditional knowledge probing.
- 
---
### Notes (Try to use backlinks)
- Giant models suffer from poor transferability. Fine-tuning on downstream tasks hardly works for those trillion-scale models.
- [[P-tuning]]
	- ![[2021_P-Tuning.png]]
- The P-tuning significantly pushes the boundary of knowledge probing from 43.3% to 50.6% in LAMA-34k and 45.2% to a maximum of 64.2% in LAMA-29k
- in terms of knowledge probing, many facts can only be hard-coded rather than inferenced by language models.
	- [[P-tuning]] does not change the pre-trained models’ parameters but evoke the stored knowledge by finding a better continuous prompt
- P-tuning shows a better affinity with unidirectional language models. In MegatronLM2 terms of much larger models such as with 11 billion parameters, while fine-tuning hardly works, P-tuning is still applicable and achieve the state-of-the-art on LAMA.
- FewGLUEis a subset of SuperGLUE, each task consisting of 32 train data and an additional unlabeled set of different size ranging from 400 to 20000
- P-tuning appears to be more beneficial in low-resource settings
- As a new paradigm of tuning pretrained models, P-tuning could search over a vast prompt space while tuning pretrained models’ parameters.
---
