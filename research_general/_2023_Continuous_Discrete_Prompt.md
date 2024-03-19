### Is Continuous Prompt a Combination of Discrete Prompts? Towards a Novel View for Interpreting Continuous Prompts
---
- [Zotero Select Link](zotero://select/groups/2480461/items/L852EYGQ)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/L852EYGQ)
- Authors: [[Tianjie Ju]]  [[Gongshen Liu]] 
- Topics: [[nlp_train]] [[nlp_prompt]] [[nlp_knowlegde_representation]]
- Venue: #arxiv #ACL
- Year: #2023

---
### Major Contributions
- we propose the Combination Hypothesis, which argues the feasibility of utilizing combinations of discrete prompts as faithful interpretations for continuous prompts (§3.2)
	- we treat the continuous prompt as an embedding lookup table with the one-hot restriction removed
	- We first directly optimize parameters of the combination of discrete prompts to replace continuous prompts.
- Results show that the combination of discrete prompts has competitive performance in most scenarios (especially in few-shot learning)
---
### Secondary Contribution
- 
---
### Limitations/Future Work
- Although the proposed method provides interpretations for continuous prompts with both faithfulness and plausibility, it can still only be used as an approximation to find the most likely combination, since the process of combining discrete prompts to continuous prompts is irreversible.
- Due to space and time constraints, we only perform detailed experiments on P-tuning and the bidirectional language models like BERT and RoBERTa
---
### Notes (Try to use backlinks)
- we investigate the feasibility of interpreting continuous prompts as the weighting of discrete prompts by jointly optimizing prompt fidelity and downstream fidelity
- Our experiments show that: 
	- (1) one can always find a combination of discrete prompts as the replacement of continuous prompts that performs well on downstream tasks; 
	- (2) our interpretable framework faithfully reflects the reasoning process of source prompts; 
	- (3) our interpretations provide effective readability and plausibility, which is helpful to understand the decisionmaking of continuous prompts and discover potential shortcuts
- **Discrete prompts** usually search for templates, i.e., natural language tokens in discrete spaces as prompt functions.
	- These methods rely excessively on prior knowledge, while even experts have difficulty finding optimal templates (Jiang et al., 2020).
- **Continuous prompts**, on the other hand, relax the constraint that templates are natural language tokens (Li and Liang, 2021; Liu et al., 2021b; Lester et al., 2021; Zhong et al., 2021; Qin and Eisner, 2021; Zhang et al., 2022).
	- These works effectively improve performance at the expense of interpretability.
- As a post-hoc interpretable framework, this paper investigates the feasibility of cross-model transfer without the help of additional task data.
- we propose the idea that the continuous prompt may be a combination of multiple discrete prompts
- **Finding Interpretations** The hypothesis indicates the existence of R, but it does not consider how to find a solution that better represents the continuous prompt.
- a simple model with only one linear layer is designed in our paper for interpreting continuous prompts
- where DKL(·) is the Kullback Leibler distance function, M (·) is the output of the PLM. This loss function helps to find a more meaningful combination, i.e., discrete prompts with larger values should have outputs on downstream tasks that are as consistent as possible with the continuous prompt
- P-tuning (Liu et al., 2021b), as a typical representative of continuous prompts, is used in this paper to study our proposed framework.
- For comparison, the two nearest tokens in the Euclidean space are selected as interpretations for continuous prompts. Among all tasks, the distance of our results from the source prompts is closer compared to the nearest discrete token, indicating that our method has a higher fidelity in the restoration of source prompts
	- Moreover, simply taking the two nearest discrete tokens as a replacement for continuous prompts performs quite poorly on downstream tasks,
- With our proposed interpretable framework that establishes connections between continuous and discrete prompts, it becomes feasible to transfer continuous prompts from source PLMs to target PLMs without extra training signals on target PLMs.
---
