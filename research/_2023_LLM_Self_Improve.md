### Large Language Models Can Self-Improve
---
- [Zotero Select Link](zotero://select/groups/2480461/items/DVP7U9E7)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/DVP7U9E7)
- Authors: [[Jiaxin Huang]] [[Jiawei Han]]
- Topics: [[nlp_agents]] [[nlp_llm]]
- Venue: #arxiv #EMNLP 
- Year: #2023

---
### Major Contributions
- we demonstrate that an LLM is also capable of self-improving with only unlabeled datasets
- [[LMSI]]
- we study how an LLM is able to self-improve its reasoning ability without supervised data. We show that using only input sequences (without ground truth output sequences) from multiple NLP task datasets, a pre-trained LLM is able to improve performances for both in-domain and out-of-domain tasks.
---
### Secondary Contribution
- We can observe that confident answers are more likely to be correct, which means that when a question has many consistent CoT paths, then the corresponding  ̃ y is more likely to be correct. On the other hand, when  ̃ y is wrong, it is likely to be supported by fewer CoT paths, and brings little noise to the training samples
- urthermore, the single path CoT-Prompting performance of LMSI is close to or even better than the multiple path Self-Consistency performance of the model without LMSI
---
### Limitations/Future Work
- “when the amount of training questions or CoT examples is limited, our method may not generate sufficient training samples for language model self-training.” (Huang et al., 2022, p. 5)
---
### Notes (Try to use backlinks)
- new capabilities have emerged from LLMs as they are scaled to hundreds of billions of parameters (Wei et al., 2022a): in-context few-shot learning (Brown et al., 2020) makes it possible for an LLM to perform well on a task it never trained on with only a handful of examples; Chain-of-Thought (CoT) prompting (Wei et al., 2022b; Kojima et al., 2022) demonstrates strong reasoning ability of LLMs across diverse tasks with or without few-shot examples
- For each model, during test time, we apply three separate prompting methods on all six datasets: standardprompting, CoT-Prompting, and Self-Consistency
- It is interesting to point out that after distillation from LMSI, the 62 billion model can outperform the pre-trained 540 billion model, and the 8 billion model can outperform the pre-trained 62 billion model. This implies that for downstream applications with limited computing resources, the reasoning knowledge from large models can be used to largely enhance small models to achieve competitive performance
- ![[2023_LLM_Self_Improve_prompts.png]]
- ![[2023_LLM_Self_Improving_architecture.png]]
- ![[2023_LLM_Self_Improve_train.png]]
---
