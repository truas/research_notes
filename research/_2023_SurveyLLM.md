### A Survey of Large Language Models
---
- [Zotero Select Link](zotero://select/groups/2480461/items/CLBC22NT)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/CLBC22NT)
- Authors: [[Wayne Xin Zhao]] [[Important Author]] [[Jin-Ron Wen]] 
- Topics: [[nlp_llm]] [[nlp_survey]]
- Venue: #arxiv
- Year: #2023

---
### Major Contributions
- Survey on LLM - on four major aspects of LLMs, namely pre-training, adaptation tuning, utilization, and capacity evaluation
---
### Secondary Contribution
- Scaling. Scaling is the key factor to increase the model capacity of LLMs
	- Further, the quality of the pre-training data plays a key role in achieving good performance, so that data collection and cleaning strategies are very important to consider when scaling the pre-training corpora.
- Ability eliciting. After being pre-trained on large-scale corpora, LLMs are endowed with potential abilities as general-purpose task solvers
- Alignment tuning. It is necessary to align LLMs with human values, e.g., helpful, honest, and harmless. For this purpose, InstructGPT [61] designs an effective tuning approach that enables LLMs to follow the expected instructions, which utilizes the technique of reinforcement learning with human feedback [61, 69].
- Tools manipulation. In essence, LLMs are trained as text generators over massive plain text corpora, thus performing less well on the tasks that are not best expressed in the form of text (e.g., numerical computation).
- LLaMA (65B version) [57], which contains approximately five times as many parameters as other models, has exhibited superior performance in tasks related to instruction following.
---
### Limitations/Future Work
- 
---
### Notes (Try to use backlinks)
- Language is essentially a complex, intricate system of human expressions governed by grammatical rules
- when the parameter scale exceeds a certain level, these enlarged language models not only achieve a significant performance improvement, but also exhibit some special abilities (e.g., incontext learning) that are not present in small-scale language models (e.g., BERT)
- Although scaling is mainly conducted in model size (with similar architectures and pre-training tasks), these large-sized PLMs display different behaviors from smaller PLMs (e.g., 330M-parameter BERT and 1.5Bparameter GPT-2) and show surprising abilities (called emergent abilities [31]) in solving a series of complex tasks. For example, GPT-3 can solve few-shot tasks through in-context learning, whereas GPT-2 cannot do well. Thus, the research community coins the term “large language models (LLM)
- Third, the development of LLMs no longer draws a clear distinction between research and engineering.
- it is mysterious why emergent abilities occur in LLMs, instead of smaller PLMs.
- emergent abilities of LLMs are formally defined as “the abilities that are not present in small models but arise in large models”, which is one of the most prominent features that distinguish LLMs from previous PLMs.
	- in-context learning
	- instruction following
	- step-by-step reasoning
- Training data: Based on their content types, we categorize these corpora into six groups: Books, CommonCrawl, Reddit links, Wikipedia, Code, and others.
- ![[2023_SurveyLLM_general.png]]
![[2023_SurveyLLM_statistics.png]]
![[2023_SurveyLLM_train_data.png]]
![[2023_SurveyLLM_pipeline.png]]
---
