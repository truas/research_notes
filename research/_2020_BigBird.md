### Big Bird: Transformers for Longer Sequences
---
- [Zotero Select Link](zotero://select/groups/2480461/items/AMRXBDZT)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/AMRXBDZT)
- Authors: [[Manzil Zaheer]] [[Avina Dubey]]
- Topics: [[nlp_transformers]] [[nlp_lm]] [[_2019_BERT]]
- Venue: #arXiv
- Year: #2020
---
### Major Contributions
- Increase the input sequence lenght to 4096
- Drop attention cost to O(n) instead of O(n²)
	- attend to all parts of the sequence
	- random keys that each query attentd to
	- a block of local neighbors
- Satisfy all theoretical preoperties of full transformers
- Extended context modelled by [[_2020_BigBird]] benefits NLP tasks
- Novel application in extraction contextual representation of genomics sequencies in DNA
---
### Secondary Contribution
- [[_2020_BigBird]] - ITC: internal transformer construction, some 'global' token attend over the entire sequence
- [[_2020_BigBird]] - ETC: external transformer construction, additional 'global' tokens such as CLS
- 
---
### Limitations/Future Work
---
### Notes (Try to use backlinks)
- The self-attention architecture does not even obey sequence order as it is permutation equivariant
- Can we achieve the empirical benefits of a fully quadratic self-attention scheme using fewer inner-products?
	- Do these sparse attention mechanisms preserve the expressivity and flexibility of the original network
- Sparse attention is as powerful as full-attention mechanism
	- there is a cost to consider sparse attention
- They use [[_2019_RoBERTa]] checkpoint to start their training
- ![[2020_BigBird_architecture]]
---
