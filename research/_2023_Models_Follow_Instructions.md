### Do Models Really Learn to Follow Instructions? An Empirical Study of Instruction Tuning
---
- [Zotero Select Link](zotero://select/groups/2480461/items/FK2Y55B7)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/FK2Y55B7)
- Authors: [[Po-Nien Kung]]  [[Nanyun Peng]] 
- Topics: [[nlp_prompt]] [[nlp_instructions]]
- Venue: #arXiv #ACL
- Year: #2023

---
### Major Contributions
- we analyze how models utilize instructions during IT by comparing model training with altered vs. original instructions. Specifically, we create simplified task definitions by removing all semantic components and only leaving the output space information, and delusive examples that contain incorrect input-output mapping.
---
### Secondary Contribution
- 
---
### Limitations/Future Work
- 
---
### Notes (Try to use backlinks)
- Models trained with task instructions demonstrate impressive zero-shot cross-task generalization ability. (Kung and Peng, 2023, p. 1317)
- “Min et al. (2022) analyze how model utilize examples in ICL. They observed that (1) Input-output mapping in examples is not important and(2) Output space information is crucial.” (Kung and Peng, 2023, p. 1317)
- ![[2023_Models_Follow_Instructions_pipeline.png]]
- “for task definition, we create simplified versions by removing all semantic components in the instructions and only leaving the output space information. For task examples, we create delusive examples with incorrect input-output mapping, where the examples’ input and output spaces are correct, but the inputoutput mappings are wrong.” (Kung and Peng, 2023, p. 1318)
- “Our experiments show that models trained with simplified task definitions achieve performances on par with the original IT models with different numbers of training examples ranging from 10 to 800 per task.” (Kung and Peng, 2023, p. 1318)
- **Instruction tuning to generalize to unseen tasks.**
	- In the first stage, the models are trained on a set of training tasks with instructions (task-definition and task-examples). After training, the models are evaluated on a set of unseen testing tasks for zero-shot generalizability
- **Instruction tuning to generalize to unseen instructions.**
- Random Guessing baseline can also achieve 42.6% exact-match score, on par with TK-Instruct trained in low resource setting (less than five instances per task). This suggests that the majority of score improvement from IT may come from model learning the output format, especially in low-resource settings.
- “To investigate their instruction utilization, we conduct the “Altered Task Definition” experiment on LLaMA-7B (Touvron et al., 2023) and Alpaca-7B models using the NatInst-V2 test set. In Table 2, training the LLaMA model on the NatInst-V2 dataset using the Original task definition leads to substantial performance enhancements than zeroshot. However, the Simplified task definition also achieves comparable performance, with a minimal decrease of 3 (EM/Rouge-L)scores” (Kung and Peng, 2023, p. 1321)
- Our findings indicate that some current IT models do not fully utilize instructions, and the impressive performance gains of IT may come from models learning superficial patterns, such as the output space and format. We suggest future research on instruction tuning to analyze their performance gains with more comprehensive evaluation and benchmark against trivial baselines
- our work is a concentrated analysis to illuminate the potential vulnerability of the current IT models and evaluation metrics.
---
