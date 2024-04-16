### Primer: Searching for Efficient Transformers for Language Modeling
---
- [Zotero Select Link](zotero://select/groups/2480461/items/5KJH6KXT)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/5KJH6KXT)
- Authors: [[David R. So]] [[Quoc V. Le]]] 
- Topics: [[nlp_transformers]] [[nlp_arch]]
- Venue: #arXiv
- Year: #2021
---
### Major Contributions
- They propose [[_2021_Primer]], a cheper alternative architecture to the traditional [[_2017_Transformer]]
	- squaring ReLU activations
	- adding depthwise convolution layer after each Q, K, and V projection in self-attention
	- Reduces training cost by x4
	- Primer -> Primitives searched Transformer
---
### Secondary Contribution

---
### Limitations/Future Work
---
### Notes (Try to use backlinks)
- Primer has the benefits of (1) achieving a target quality using a smaller training cost, (2) achieving higher quality given a fixed training cost, and (3) achieving a target quality using a smaller inference cost. ->this stand across wide range in hyperparameters, compute scale, datasets, hardware, etc
- We also find that wider depthwise convolution and standard convolution not only do not improve performance, but in several cases hurt it. Although depthwise convolutions have been used for Transformers before 
- In Appendix A.12, we perform encoder-decoder masked language modeling comparisons in T5, but do not study the results in significant depth. The main finding there is that, although Primer modifications improve upon vanilla Transformer, they perform only as well as Transformer++. This result suggests that architectural modifications that work well for decoder-only auto-regressive language models may not necessarily be as effective for encoder-based masked language models.
- ![[2021_Primer_Proposal_general.png]]
- 
---
