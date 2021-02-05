### DeBERTa: Decoding-Enhanced BERT with Distangled Attention
---
- [Zotero Select Link](zotero://select/groups/2480461/items/R8JXIQF9)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/R8JXIQF9)
- Authors: [[Pengcheng He] [[Weizhu Chen]]
- Topics: [[nlp_transformers]] [[nlp_attention]] [[ann_architecture]]
- Venue: #arXiv 
- Year: #2021
---
### Major Contributions
- [[_2021_DeBERTa]] is an improvment of [[_2019_BERT]] and [[_2019_RoBERTa]]
	- distangled attention mechanism and improved mask decoder
---
### Secondary Contribution
- we scale up [[_2021_DeBERTa]] by training a larger version that consists of 48 Transform layers with 1.5 billion parameters. The significant performance boost makes the single DeBERTa model surpass the human performance on the SuperGLUE benchmark
- we propose the [[SiFT|Scale-invariant-Fine-Tuning]] algorithm that improves the training stability by applying the perturbations to the normalized word embeddings. 
	- Specifically when fine-tuning DeBERTa to a downstream NLP task in our experiments, SiFT first normalizes the word embedding vectors into stochastic vectors, and then applies the perturbation to the normalized embedding vectors.
	- 
---
### Limitations/Future Work
 - the distangled attention does not seem that innovative, instead of summing the content-position they used their vectors separately
 - 6 DGX-2 machines (96 V100 GPUs) to train the models. A single model trained with 2K batch size and 1M steps takes about 20 days.
---
### Notes (Try to use backlinks)
- **distangled attention** - DeBERTa is represented using two vectors that encode its content and position, respectively, and the attention weights among words are computed using disentangled matrices based on their contents and relative positions, respectively.
- **Enhanced mask decoder** - DeBERTa incorporates absolute word position embeddings right before the softmax layer where the model decodes the masked words based on the aggregated contextual embeddings of word contents and positions
	- DeBERTa, we incorporate them right after all the Transformer layers but before the softmax layer for masked token prediction
-  The standard self-attention mechanism lacks a natural way to encode word position information
	-  relative position representations are more effective for natural language understanding and generation tasks
-  the attention weight of a word pair can be computed as a sum of four attention scores using disentangled matrices on their contents and positions as content-to-content, content-to-position, position-to-content, and position-to-position

---
