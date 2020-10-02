### Rethinking Attention With Performers
---
- [Zotero Select Link](zotero://select/groups/2480461/items/BCG9B65S)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/BCG9B65S)
- Authors: [[Krzysztof Choromanski]] [[Adrian Weller]]
- Topics: [[nlp_transformers]] [[nlp_attention]]
- Venue: #arXiv
- Year: #2020
---
### Major Contributions
- Build on top of[[ FAVOR+|Fast Attention Via Positive Orthogonal Random features]]
- [[_2020_Performer]] a are linear architectures fully compatible with regular [[_2017_Transformer]] and with strong theoretical guarantees: unbiased or nearly-unbiased estimation of the attention matrix, uniform convergence and low estimation variance
- Use/proposal of [[FAVOR+]] - independent of interest
	- Estimates softmax (and Gaussian) kernels with positive orthogonal random features which [[FAVOR+]] leverages for the robust and unbiased estimation of regular (softmax) attention and show how FAVOR+ can be applied for other attention-kernels
---
### Secondary Contribution
---
### Limitations/Future Work
---
### Notes (Try to use backlinks)
- Linear space and time complexity
- Regular approaches deal with the quadratic cost of attention restricting the attention neighborhood or using low-rank kernels
- Approximations based on truncated back-propagation (Dai et al., 2019) are also unable to capture long-distance correlations since the gradients are only propagated inside a localized window.
- ![[2020_Performer_attention.png]]
- Extremely dense paper.... need more reading
---
