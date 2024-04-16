### The Depth -to-Width Interplay in Self-Attention
---
- [Zotero Select Link](zotero://select/groups/2480461/items/IFVERJQX)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/IFVERJQX)
- Authors: [[Yoav Levine]] [[Ammon Shashua]] 
- Topics: [[nlp_attention]] [[nlp_lm]] [[nlp_training]]
- Venue: #NIPS #arXiv
- Year: #2021
---
### Major Contributions
- We conduct systematic empirical ablations on networks of depths 6 to 48 that clearly reveal the theoretically predicted behaviors, and provide explicit quantitative suggestions regarding the optimal depth-to-width allocation for a given self-attention network size.
	- our theoretical analysis is the first to address the question of parameter allocation between depth and width in self-attention networks.
---
### Secondary Contribution
---
### Limitations/Future Work
---
### Notes (Try to use backlinks)
- in contrast to the depth “arms race" that took place in the ConvNet case, the leading self-attention networks are not much deeper than the original BERT model
- depth may not play as crucial a role in self-attention networks as it does in convolutional networks
-  Our results clearly show that the optimal path towards the 1-Trillion parameter mark includes massive widening.
-  GPT3-175B, is too deep given its size, and could have benefited from widening at the expense of depth (similarly to the depth network in the gray regime of figure 2(c). We project that the strongest 1-Trillion parameter 48 model would entail widening to an unprecedented width of 30K.
-  the operation of stacking self-attention layers is so effective that it quickly saturates a capacity of the network’s width.
-  Empirical evidence indicates that while the ReLU activations and softmax normalization contribute to performance (layer-norm mainly contributes to optimization), the basic mechanism in eqs. (3) and (4) above captures the defining delf-attention characteristic of integrating the inputs with each other in a flexible manner
---
