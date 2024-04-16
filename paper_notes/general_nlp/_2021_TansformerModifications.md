### Do Transformer Modifications Transfer Across Implementations and Applications?
---
- [Zotero Select Link](zotero://select/groups/2480461/items/TW9TVRET)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/TW9TVRET)
- Authors: [[Sharan Narang]] [[Colin Raffel]]
- Topics: [[nlp_survey]] [[nlp_transformers]]
- Venue: #arXiv
- Year: #2021
---
### Major Contributions
- why most modifications proposed to the Transformer have not seen widespread adoption.
	- many Transformer modifications do not result in improved performance in our experimental setting
	- Transformer modifications exhibit a surprising lack of generalization across different implementations and tasks.
- we comprehensively evaluate many Transformer modications in a shared experimental setting that covers most of the common uses of the Transformer in natural language processing
	- performance improvements may strongly depend on implementation details
---
### Secondary Contribution
---
### Limitations/Future Work
---
### Notes (Try to use backlinks)
- many modifications to the Transformer architecture have been proposed. However, the most widely-used applications of the Transformer architecture (e.g. Devlin et al. (2018); Yang et al. (2019); Radford et al. (2018); Rael et al. (2019)) incorporate few of these modifications
- modifcations proposed to the Transformer do not generalize across applications, i.e. the modifications only help on the limited experimental setting considered when the modification was proposed, and/or rely on specific details that are not common across implementations of the Transformer.
- **Modifications**
	- *Activations* - ReLU
		- [[GeLU]],[[Swish]], [[ELU]], [[SeLU]], [[Sigmoid]], [[Softplus]], [[GLU]] variations
	- *Normalization* - [[RMS|root-mean-square]]  and [[Fixup]]
	- *Depth* - trade-offs between the width of the feedforawrd blocks and depth
	- *Embeddings* -  tying only encoder input and decoder input embeddings, tying only decoder input and output embeddings, and untying all the embeddings; we explored factorizing the embedding matrix into two smaller matrices
	- *Parameter sharing* - we explored sharing the parameters of the Transformer layers inspired by the ALBERT model of Lan et al. (2020). - Factorize embeddings, Shared embeddings
	- *Softmax* - variations of softmax - Adaptative Softmax, Mixture of Softmaxes, 
	- *Architectures* - Transparent attention, Evolved Transformer, Synthesizer variants (factorized,dense, and random Synthesizer variants), Funnel Transformer, Lightweight and Dynamic convolutions, Sparse Expert Transformers (Mixture of Experts Transformer, Switch Transformers), Product Key Memory, Universal Transformer,
	- 
---
