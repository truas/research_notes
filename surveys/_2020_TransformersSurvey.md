### Efficient Transformers: A Survey
---
- [Zotero Select Link](zotero://select/groups/2480461/items/HF7B8SJU)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/HF7B8SJU)
- Authors: [[Yi Tay]] [[Donald Metzler]]
- Topics: [[nlp_survey]] [[nlp_transformers]]
- Venue: #arXiv
- Year: #2020
---
### Major Contributions
- Focus on modeling advances and architectural innovations that tackle the quadratic complexity in self-attention
- 
---
### Secondary Contribution
---
### Limitations/Future Work
---
### Notes (Try to use backlinks)
- Quadratic time and memory complexity in the attention mechanism asks for optimization
- Efficiency can be: memory footprint, number of FLOPs, cost, parameters, etc
- ![[2020_TranformersSurvey_TransArch.png]]
- The multihead attention can be calculated in parallel
	- The self-attention A=QK^T - dot product between Query and K - O(n^2) (time and memory)
- Uses of Transformers: 
	- encoder-only (classification)
	- decoder-only (language modeling)
	- encoder-decoder (translation): multi-head-self-attention
- ![[2020_TransfomersSurvey_Taxonomy.png]]

- Fixed Patterns: sparsify the attention matrix
	- Blockwise: Chunking the input - Blockwise (Qiu 2019), Local Attention (Parmar 2018)
	- Strided: atten to fixed intervals - Sparse Transformer (Child 2019); Longformer (Beltagy 2019)
	- Compressed: pooling operator to down sample sequence length to be a form fixed pattern - Memory Compressed Attention (Liu 2018)
- Combination: combine distinct approaches - Axial Transformer (Ho 2019)
- Learnable: learn access patterns in data-driven fashion. A key characteristic of learning patterns is to determine a notion of token relevance and then assign tokens to buckets or clusters. Similarity function is trained end-to-end jointly  with the rest of the network - Reformer (Kitaev 2020); Routing Transformer (Roy 2020); Sinkhorn Sorting Network (Tay 2020);
- Memory: leverage side memory module that can access muktiple tokens at once. A common form is global memory which is able to access the entire sequence - Set Transformers (Lee 2019)
- Low Rank Methods: improve efficiency by leveraging low-rank approximations of the self-attention matrix N x N -> N x k - Linformer (Wang 2019)
- Kernels: apply kernels to rewrite the attention mechanisms - Linear Transformer (Katharopoulos 2020); Performer (Choromanski 2020)
- Recurrence: Extension to the blockwise methods (connect these blocks via recurrence) - Transformer-XL
-
---
