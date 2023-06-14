### Decomposition Enhances Reasoning via Self-Evaluation Guided Decoding
---
- [Zotero Select Link](zotero://select/groups/2480461/items/CURYCNL7)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/CURYCNL7)
- Authors: [[Yuxi Xie]]  [[Qizhe Xie]] 
- Topics: [[nlp_prompt]] [[nlp_llm]]
- Venue: #arxiv
- Year: #2023

---
### Major Contributions
- We propose an effective prompting approach that integrates self-evaluation guidance through stochastic beam search.
- [Link](https://github.com/YuxiXie/SelfEval-Guided-Decoding)
- 
---
### Secondary Contribution
- Sampling Diversity. We examine the influence of sampling diversity on the final performance and the significance of hyperparameters associated with sampling diversity. It is clear that more diversity resulting from higher temperatures (including both τ and γ) generally leads to a decline in performance when only considering one run. However, diversity significantly benefits majority voting on multiple reasoning chains.
---
### Limitations/Future Work
- 
---
### Notes (Try to use backlinks)
- breaking down a problem into intermediate stages, or a reasoning chain, can significantly improve model performance on reasoning tasks (Cobbe et al., 2021).
- the complexity and length of reasoning chains increase with the difficulty of tasks, LLMs struggle with errors and imperfections that accumulate across multiple intermediate steps (Wu et al., 2016; Guo et al., 2018; Chen et al., 2022)
- ![[2023_Self_Eval_Decoding_example.png]]
- we formulate the generation of the reasoning chain as a decoding process consisting of a sequence of intermediate steps.
	- we consider each decoding step as a reasoning logic composed of a sequence of tokens. This framework enables us to employ beam search (Jurafsky and Martin, 2009; Graves, 2012) decoding tailored for intermediate steps and guide the beam searching process by controlling the error of each reasoning step to prevent potential error accumulation throughout the chaining.
	- we employ LLM self-evaluation (Kadavath et al., 2022) as an automatic criterion to offer the guiding signal, drawing inspiration from prior works on utilizing LLMs for self-evaluation (Rae et al., 2021
- ![[2023_Self_Eval_Decoding_framework.png]]
- we propose a constrained stochastic beam search decoding approach to improve the faithfulness of each reasoning step and obtain high-quality reasoning with a limited number of samples.
---
