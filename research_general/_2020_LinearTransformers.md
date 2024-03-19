### Transformers are RNNs: Fast Autoregressive Transformers with Linear Attention
---
- [Zotero Select Link](zotero://select/groups/2480461/items/GN8AKUSI)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/GN8AKUSI)
- Authors: [[Angelos Katharopoulos]] [[Fraçois Fleuret]] [[Apoorv Vyas]]
- Topics: [[nlp_attention]] [[ann_architecture]] [[nlp_transformers]]
- Venue: #ICML
- Year: #2020
---
### Major Contributions
- Approximate the self-attention to O(N) instead of O(N^2): Linear Transformer
	- self-attention as a linear dot-product of kernel features maps approximating the transformers to a RNN
	- For the image datasets the improvement is around 4000x (time)
- Linear Transformers does not carry the restrictions from [[_2020_Reformer]]
- [Linear Transforrmers](https://linear-transformers.com/)
---
### Secondary Contribution
- Approximate their softmax to a linear dor product of feature maps
- they evaluate their linear transformer into MNIST, CIFAR-10 and Speech Recognitions - high robstuness in their approach
- 
---
### Limitations/Future Work
---
### Notes (Try to use backlinks)
- Approaches to improve efficiency (memory) in transformers:
	- weight pruning (Michel 2019)
	- weight quantization (Zafrir 2019)
	- weight factorization (Lan 2019)
	- knowledge distillation (Lample 2019)
- (Child 2019) O(N.sqrt.N)
- (Kitaev 2020) O(N.log.N) [[_2020_Reformer]] [[LSH]]
	- Requires the keys to be identical to the queries - allowing only for encoding
- Linear transformer model combines the best of both worlds. 
	- Train - the computations can be parallelized and take full advantage of GPUs or other accelerators. 
	- Infference - the cost per time and memory for one prediction is constant for their model.
---
