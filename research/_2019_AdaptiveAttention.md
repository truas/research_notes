### Adaptive Attention Span in Transformers
---
- [Zotero Select Link](zotero://select/groups/2480461/items/Z9ADTE8W)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/Z9ADTE8W)
- Authors: [[Sainbayar Sukhbaatar]] [[Piotr Bojanowski]] [[Armand Joulin]]
- Topics: [[nlp_transformers]]	[[nlp_attention]] [[nlp_cost]]
- Venue: #ACL
- Year: #2019
---
### Major Contributions
- New adaptative attention mechanism that allows for long sequences, stable FLOPS, and improve performance
	- use relative position embeddings (Shaw et al 2018)
	- caching mechanism (Dai et al 2019)
- Not all attention heads are used throughout the entire sequence
---
### Secondary Contribution
---
### Limitations/Future Work
---
### Notes (Try to use backlinks)
- Adaptive attention: for each head they add a masking functions to control for the span of attention
	- This soft-masking is a result from [[_2017_VariableComputation_RNN]]
- Dynamic attention span: dynamic computation approach, where the attention span change based on the current input [[_2016_ACT]] (Adaptive Computation time for RNN)
- Smaller attention span has a direct impact on the total number of FLOPS for computation of one-step prediction
- ![[2019_AdaptiveAttention_results.png]]
- 
---
