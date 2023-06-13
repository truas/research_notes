### Tree of Thoughts: Deliberate Problem Solving with Large Language Models
---
- [Zotero Select Link](zotero://select/groups/2480461/items/H6FQFV6D)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/H6FQFV6D)
- Authors: [[Shunyu Yao]] [[Karthik NArasimhan]] 
- Topics: #nlp_instruction #google_deepmind
- Venue: #arxiv
- Year: #2023

---
### Major Contributions
- “Tree of Thoughts” (ToT) [[Tree of Thoughts|ToT]], which generalizes over the popular “Chain of Thought” approach to prompting language models, and enables exploration over coherent units of text (“thoughts”) that serve as intermediate steps toward problem solving
	- ToT allows LMs to perform deliberate decision making by considering multiple different reasoning paths and self-evaluating choices to decide the next course of action, as well as looking ahead or backtracking when necessary to make global choices.
- A specific instantiation of [[ToT]] involves answering four questions:
	- How to decompose the intermediate process into thought steps; 
	- How to generate potential thoughts from each state;
	- How to heuristically evaluate states;
	- What search algorithm to use.
- [link](https://github.com/princeton-nlp/tree-of-thought-llm)
---
### Secondary Contribution
- 
---
### Limitations/Future Work
- search methods like ToT requires more resources (e.g. GPT-4 API cost) than sampling methods in order to improve task performances, but the modular flexibility of ToT allows users to customize such performance-cost tradeoffs, and ongoing open-source efforts [29] should readily reduce such costs in the near future
- this work focuses on using an off-the-shelf LM, and fine-tuning LMs using a ToT-style high-level counterfactual decision making (e.g. deliberating over potential choices for the next paragraph, instead of predicting the next token) might present opportunities to enhance the problem-solving capabilities of LMs
---
### Notes (Try to use backlinks)
- It is perhaps surprising that underlying all this progress is still the original autoregressive mechanism for generating text, which makes token-level decisions one by one and in a left-to-right fashion
- We thus propose the Tree of Thoughts (ToT) framework for general problem solving with language models.
- we combine this language-based capability to generate and evaluate diverse thoughts with search algorithms, such as breadth-first search (BFS) or depth-first search (DFS), which allow systematic exploration of the tree of thoughts with lookahead and backtracking.
- ![[2023_Tree_of_Thought_process.png]]
- Empirically, we propose three new problems that challenge existing LM inference methods even with the state-of-the-art language model, GPT-4 [20]: Game of 24, Creative Writing, and Crosswords
- **two key shortcomings** of existing approaches that use LMs to solve general problems: 1) Locally, they do not explore different continuations within a thought process – the branches of the tree. 2) Globally, they do not incorporate any type of planning, lookahead, or backtracking to help evaluate these different options – the kind of heuristic-guided search that seems characteristic of human problem-solving.
- Self-reflection. Using LLMs to assess the viability of their own predictions is becoming an increasingly important procedure in problem solving.
---
