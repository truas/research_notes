### Let Models Speak Ciphers: Multiagent Debate Through Embeddings
---
- [Zotero Select Link](zotero://select/groups/2480461/items/KF36BBB8)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/KF36BBB8)
- Authors: [[Chau Pham]] [[Important Author]] [[Hongxia Yang]] 
- Topics: [[nlp_agent]] [[nlp_debate]] [[nlp_embeddings]]
- Venue: #arxiv #ICLR
- Year: #2024

---
### Major Contributions
- “we introduce a communication regime named [[CIPHER]] (Communicative Inter-Model Protocol Through Embedding Representation) to address this issue. Specifically, we remove the token sampling step from LLMs and let them communicate their beliefs across the vocabulary through the expectation of the raw transformer output embeddings.” (Pham et al., 2024, p. 1)
	- “[[CIPHER]] offers an advantage of encoding a broader spectrum of information without any modification to the model weights, outperforming the state-of-the-art LLM debate methods using natural language by 0.5 − 5.0% across five reasoning tasks and multiple open-source LLMs of varying sizes” (Pham et al., 2024, p. 1)
		- 	“[[CIPHER]] bypasses the token sampling process by generating the weighted average of all tokens’ embeddings in the vocabulary set, instead of yielding a single token. Thus, this passes richer information to other models during debate, particularly when the model is uncertain.” (Pham et al., 2024, p. 2)
	- “We validate this claim by evaluating our approach on five diverse datasets across multiple domains: GSM8K (Cobbe et al., 2021), Arithmetic (Du et al., 2023), MMLU Formal Logic, MMLU High School Math, and MMLU Professional Psychology (Hendrycks et al., 2020).” (Pham et al., 2024, p. 2)
---
### Secondary Contribution
-  “CIPHER benefits the most when it pairs a low-temperature agent with a high-temperature one. At higher temperatures, the probability distribution of the tokens in the vocabulary becomes more uniform, allowing CIPHER’s responses to lean towards less confident token choices.” (Pham et al., 2024, p. 8)
- “For CIPHER (bottom row), the optimal regions appear on the left side of the charts, where temperature 1 is lower than temperature 2. These indicate that a good strategy is using various temperature agents, and choosing the response of the lower temperature agent as the final debate answer. See Section 5.2 for more discussion.” (Pham et al., 2024, p. 9)
---
### Limitations/Future Work
- Not understanding the intermediate steps plays against interpretable models
- “we find that our approach can generalize across a wide array of LLMs, enabling even smaller LLMs to unlock the benefits of debate and achieve better performance than majority voting (Wang et al., 2023b). This suggests that, even for open-source models, debate is still an efficient form of communication to boost the performance of LLMs.” (Pham et al., 2024, p. 2)
	- This can be an interesting selling point to use the approach - assuming that just a handfull of results are observed in larger models, such as GPT4
- What happens when the word representation is done via subwords?
---
### Notes (Try to use backlinks)
- “Although natural language is an obvious choice for communication due to LLM’s language understanding capability, the token sampling step needed when generating natural language poses a potential risk of information loss, as it uses only one token to represent the model’s belief across the entire vocabulary” (Pham et al., 2024, p. 1)
- “To leverage LLM’s language understanding capability, prior work (Du et al., 2023; Liang et al., 2023) adopted natural language during debates. Using natural language for debate is appealing due to its interpretability, but we argue that natural language is neither necessary nor optimal for inter-LLM communication” (Pham et al., 2024, p. 1).
- “Self-improvement via feedback. Madaan et al. (2023) presented a self-improvement framework, where an LLM doubles as both generator and critic. While this approach allows models such as GPT-3.5 and GPT-4 to boost performance, it falters for smaller and less competent models such as Vicuna-13B (Chiang et al., 2023), which struggled on consistently generating feedback in the required format.” (Pham et al., 2024, p. 3)
- ![[2024_Multiagent_Debate_Embeddings_CIPHER.png]]
- “While using one token at each position is useful for humans to understand the outputs from LLMs, we posit that it is not a requirement for effective inter-LLM communication.” (Pham et al., 2024, p. 4)
- “Thus, we argue that the token sampling process, which sacrifices information for readability, may lead to a sub-optimal solution for inter-LLM communication.” (Pham et al., 2024, p. 4)
- “Our goal is to encode as much information as possible during inter-LLM communication. However, LLMs are designed to understand natural language sequences. Thus, they might not be able to grasp vectors that reside outside the convex hull of the tokenizer’s embedding space.” (Pham et al., 2024, p. 4)
- “Table 1 presents the results from debates between two identical LLaMA family LLMs operating at different temperatures. Both Self-Consistency (Major@5) and NLD (Du et al., 2023) exhibit significant performance enhancements over a single answer. Remarkably, CIPHER consistently outperforms both baselines, achieving a 1.0 − 5.0% boost over NLD across all datasets.” (Pham et al., 2024, p. 6)
- “a) Number of rounds. In general, adding more rounds helps to boost performance on both CIPHER and NLD (Du et al., 2023).” (Pham et al., 2024, p. 8)
- “We employ Bayesian optimization (Nogueira, 2014) to identify promising pairs of temperatures in debates between two LLaMA2-70B debaters on Arithmetic dataset. Unlike the final response aggregation strategy in CIPHER, we evaluate the effectiveness of these temperature pairs based on the accuracy of the final response from the first debater (temperature 1), which can operate at a higher temperature. Such an experiment setting not only sheds light on the impact of temperature selection on debate performance but also guides our final response aggregation strategy.” (Pham et al., 2024, p. 8)

---
