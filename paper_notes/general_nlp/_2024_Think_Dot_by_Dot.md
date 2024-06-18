### Let’s Think Dot by Dot: Hidden Computation in Transformer Language Models
---
- [Zotero Select Link](zotero://select/groups/5566776/items/4B7AYV7Q)
- [Zotero URI](https://www.zotero.org/groups/5566776/items/4B7AYV7Q)
- Authors: [[Jacob Pfau]]  [[Samuel R. Bowman]] 
- Topics: [[nlp_reasoning]] [[nlp_llm]]
- Venue: #arxiv
- Year: #2024

---
### Major Contributions
- The fact that intermediate tokens can act as filler tokens raises concerns about large language models engaging in unauditable, hidden computations that are increasingly detached from the observed chain-of-thought tokens.
- [GitHub](https://github.com/JacobPfau/fillerTokens)
- “we demonstrate that transformers trained on the next-token prediction objective can achieve improved performance on certain tasks when given filler tokens, achieving perfect accuracy whereas the no-filler, immediate-answer setting achieves only low accuracy.” (Pfau et al., 2024, p. 2)
---
### Secondary Contribution
- 
---
### Limitations/Future Work
- “Thus, unlike for chain of thought, we cannot expect filler tokens to let transformers solve problems outside TC0, e.g. graph connectivity.” (Pfau et al., 2024, p. 2)
---
### Notes (Try to use backlinks)
- “Chain-of-thought responses from language models improve performance across most benchmarks. However, it remains unclear to what extent these performance gains can be attributed to human-like task decomposition or simply the greater computation that additional tokens allow” (Pfau et al., 2024, p. 1)
	- We show that transformers can use meaningless filler tokens (e.g., ‘......’) in place of a chain of thought to solve two hard algorithmic tasks they could not solve when responding without intermediate tokens. However, we find empirically that learning to use filler tokens is difficult and requires specific, dense supervision to converge.
	- “additional tokens can provide computational benefits independent of token choice.” (Pfau et al., 2024, p. 1)
- “However, recent empirical work shows that answers arrived at via chains of thought frequently are not faithful to the intermediate reasoning steps taken within the chain (Lanham et al., 2023; Turpin et al., 2023)” (Pfau et al., 2024, p. 1) - **cool**
- “Empirically, commercial large language models (LLMs) do not benefit from filler tokens on common QA and math benchmarks; Claude 2 and GPT-3.5 achieve the same performance with filler tokens as they do when responding directly without intermediate tokens (Sachan, 2023; Lanham et al., 2023).” (Pfau et al., 2024, p. 2)
- “chain of thought, in addition to providing a particular decomposition hint for a complex problem, expands the computational power of transformers in a way that is essential for many types of sequential reasoning problems.” (Pfau et al., 2024, p. 4)
- “Figure 4: To verify that filler tokens are being used for hidden computation relevant to the final 3SUM prediction, we freeze model weights and finetune only the final attention layer to predict the 3SUM task given reduced numbers of filler tokens. Accuracy improves given access to additional filler tokens, suggesting that filler token representations encode hidden computation relevant to the 3SUM prediction task. The model was trained on length-14, dimension-3 3SUM instances, and originally trained on sequences having 184 filler tokens.” (Pfau et al., 2024, p. 8)
- “To show that filler tokens confer greater expressive capacity, letting transformers solve hard problems, we must show that transformers without filler cannot solve our task, 3SUM” (Pfau et al., 2024, p. 8)
	- “To this end, we show that for short enough inputs, 3SUM can be solved without filler tokens, but for longer inputs, 3SUM cannot be solved without filler tokens. The length and dimension scaling experiments below were trained on a 50/50 split of filler and chain-of-thought data. In the below experiments, Figure 2 and Figure 5, we consider two cases:” (Pfau et al., 2024, p. 8)
- “In Figure 4, the first half of the filler tokens appear crucial, achieving 98% performance while using only 60% of the total filler tokens.” (Pfau et al., 2024, p. 9)
- “Despite transformers having the expressive capacity to solve certain filler-token tasks, learning filler token computations poses a hard learning problem. There are two reasons for this: First, it is impossible to densely supervise filler token solutions, because by assumption, filler tokens are used in precisely those cases when underlying, hidden computation decorrelates from the meaning of the corresponding tokens. Second, algorithms learned from chain-ofthought data generically require instance-adaptive, serial computation (Merrill & Sabharwal, 2023c)–such computation is incompatible with the parallel structure of filler-token compute” (Pfau et al., 2024, p. 10)
## Discussions notes
- The filler tokens are no helpful in complex tasks (>TC0)?
- What about subjective tasks do we see the same behaviour?
- In our paraphrase paper did we check if the paraphrase were introducing more tokens for the task computation?
- Having more (interpretable) tokens is suppose to help humans not machines
- How often on in what circumnstances having CoT provides wrong rational but correct answers? If there a systematic study on this?
- 
---
