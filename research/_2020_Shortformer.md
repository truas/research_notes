### Shortformer: Better Language Modeling using Shorter Inputs
---
- [Zotero Select Link](zotero://select/groups/2480461/items/3C6D5F88)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/3C6D5F88)
- Authors: [[Ofir Press]] [[Noah Smith]] [[Mike Lewis]]
- Topics: [[nlp_lm]] [[nlp_transformers]] [[ann_architecture]]
- Venue: #arXiv
- Year: #2020
---
### Major Contributions
- initially training the model on short sub sequences, before moving on to longer ones, both reduces overall training time and, surprisingly, gives a large improvement in perplexity. [[Staged Training]]
- longer subse uences perform better during na¨ive evaluation not because they are better at modeling, but because they divide the evaluation set into longer subsequences [[Early Token Curse]]
- [[Position-Infused Attention]] - This approach interferes with conventional absolute position embeddings in a way that forced Dai et al. to introduce relative position embeddings, which are computationally expensive. We introduce a fast, simple alternative: instead of adding absolute position embeddings to the word embeddings—thereby entangling a word’s content and positional information-we add them to the keys and queries in the self-attention mechanism (but not to the values)
- We propose a two-stage training routine that initially uses short input subsequences followed by long subsequences. This method was previously applied to speed up the training [[_2019_BERT]], but here we thoroughly study it and reveal that it also improves perplexity - Wiki103 (dataset)
---
### Secondary Contribution
- 
---
### Limitations/Future Work
---
### Notes (Try to use backlinks)
- we see negligible improvement between the models trained with subsequence lengths of 1,024 and 3,072 tokens (0.05 perplexity).
- long contexts may not be beneficial to transformer language models, but very short contexts are harmful.
---
