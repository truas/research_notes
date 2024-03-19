### Prompt-Based Monte-Carlo Tree Search for Goal-oriented Dialogue Policy Planning
---
- [Zotero Select Link](zotero://select/groups/2480461/items/KPJ93CK4)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/KPJ93CK4)
- Authors: [[Xiao Yu]]  [[Zhou Yu]] 
- Topics: [[nlp_llm]] [[nlp_dialogue]]
- Venue: #arxiv #EMNLP
- Year: #2023

---
### Major Contributions
- We introduce GDP-ZERO, an approach using Open-Loop MCTS to perform goal-oriented dialogue policy planning without any model training.GDP-Z ERO prompts a large language model to act as a policy prior, value function, user simulator, and system model during the tree search.
	- we contribute a novel approach to Goal-oriented Dialogue Planning with Zero training (GDP-ZERO). [[GDP-ZERO]] prompts a large language model (LLM) to perform planning by simulating future dialogue interactions (Figure 1), making it particularly suitable for tasks which would otherwise require high-quality conversations and annotations
---
### Secondary Contribution
- 
---
### Limitations/Future Work
- 
---
### Notes (Try to use backlinks)
- we treat policy planning as a stochastic game, and use prompting for every stage of an open-loop tree search. We evaluate GDP-ZERO on PersuasionForGood due to its difficult planning task (Wang et al., 2019), and find its responses are preferred over ChatGPT in both static and interactive evaluations.
- uilding on findings from Chen et al. (2023b), our approach has two main differences from existing policy planning work: we use few-shot prompting to bypass the need for model training on noisy data, and we use Open-Loop MCTS to reduce compounding simulation errors by continuously re-generating system and user responses during the tree search.
---
