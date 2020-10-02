### Linformer: Self-Attention with Linear Complexity
---
- [Zotero Select Link](zotero://select/groups/2480461/items/69JHTZQY)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/69JHTZQY)
- Authors: [[Sinong Wang]] [[Hao Ma]]]
- Topics: [[nlp_transformers]] [[nlp_attention]]
- Venue: #arXiv 
- Year: #2020
---
### Major Contributions
- A self-attention mechanism which reduces the overall complexity from O(n^2) to  O(n) for time and space
- The decompose the original scaled dot-product attention into multiple smaller attentions through linear projections, such that the combination of these operations forms a low-rank factorization of the original attention
	- The main idea of our proposed linear self-attention is to add two linear projection matrices Ei, Fi (belongs) R when computing key and value.
- Effect of sharing projections: it is possible to decrease the number of additional parameters in the model by reducing the projection matrices
- Effect of longer sequences: increases linearly
---
### Secondary Contribution
- Nice organization of related work in optimizing attention (for citation check the actual paper):
	- Mixed precision
	- Knowledge distillation
	- Sparse attention
	- LSH Attention
	- Improving Optimizar Efficiency
- Additional techniques for efficiency on top of [[_2020_Linformer]]
	- Parameter sharing between projections (headwise, key-value, layerwise)
	- Nonuniform porjected dimension
	- General projections: mean, max pooling, convolution
---
### Limitations/Future Work
---
### Notes (Try to use backlinks)
- Can Transformer models be optimized to avoid O(n^2) or is this operation required to maintain strong performance?
	- Previous techniques introduce sparsity into attention layers by having each token attend to a sub-set of tokens in the whole sequence -> this reduces the overall complexityof the attention mechanism to O(n*sq(n)), however there is performance drop with small efficiency gain (ca. 2%) - REF: Child et al 2019; Qiu et al 2019.
	- [[_2020_Reformer]] presents another, more efficient, approach ([[LSH]]) reducing the complexity even more. However its gains are only worth it for long sequences (>2048)
- the stochastic matrix formed by self-attention can be approximated by a low-rank matrix
- [[_2020_Linformer]] trained on the same corpus as [[_2019_BERT]] : BookCorpus and  Wikipedia
- ![[_2020_Linformer_attention_complexity.png]]
- They apply singular value decomposition into P across different layers and different heads of the model, and plot the normalized cumulative singular value averaged over 10k sentences. The results exhibit a clear long-tail spectrum distribution across each layer, head and task. This implies that most of the information of matrix P
can be recovered from the first few largest singular values.
	- This SVD investigation apparently inspired the [[_2020_Performer]] the idea is the same. using the K, V, Q vectors-matrices
-![[2020_Linformer_architecture.png]]
- the performance of Linformer model is mainly determined by the projected dimension k
instead of the ratio n/k
---
