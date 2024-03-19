### Augmenting Self-attention with Persistent Memory
---
- [Zotero Select Link](zotero://select/groups/2480461/items/ZZE7VLWH)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/ZZE7VLWH)
- Authors: [[Sainbayar Sukhbaatar]] [[Edouard Grave]] [[Armand Joulin]]
- Topics: [[nlp_transformers]] [[nlp_cost]] [[ann_architecture]]
- Venue: #arXiv 
- Year: #2019
---
### Major Contributions
- They propose a new models that integrates the feed-forward layers to the attention one in a single unit (all-attention)
	- feed-forward is removed -> no degradation in performance
- They replace the ReLU non-linear functions in the FFNN by a softmax and remove the biases terms
- They introduce _persistent vectors_ - which applied the attention mechanism simultaneously on the sequence of input vectors, as in the standard self-attention layer, and on a set of vectors not conditioned on the input.
	- These are shared across the data and forms a "persistent" memory similar to FFNN
---
### Secondary Contribution
- Summary on things that worked:
	- Relative position embeddings and caching [[_2019_Transformer-XL]]
	- Adaptative context size from [[_2019_AdaptiveAttention]]
	- Adaptative input and output [[_2017_EfficientSoftmax]]
	- 
---
### Limitations/Future Work
---
### Notes (Try to use backlinks)
- Architecture
- ![[2019_AugmentingSelfAttention_architecture.png]]
- This paper points out nice approaches that were considered to improve peformance under the language modeling + transformers
- Types of position encode: fixed absolute, learned absolute, learned relative
- Experiments were done on #enwik8 and #text8 - and - #WikiText-103
- Look the papers for the parameter details, they are well illustrated
- Ablation study summary:
	- (i)“all-attn” outperforms “attn-split”, which indicates that there is a
benefit in computing attention jointly over persistent and context vectors;
	- (ii) “single-head” is worse than “attn-split”, which means persistent vectors with more heads are better;
	- (iii) dividing the heads into context-only and persistent-only groups does not work well; and
	- (iv) “FF-attn” does not work as good as “all-attn” which means the switch from ReLU to Softmax alone is not sufficient
	
---
