### Longformer: The Long-Document Transformer
---
- [Zotero Select Link](zotero://select/groups/2480461/items/4FSEM9ZX)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/4FSEM9ZX)
- Author: [[Iz Beltagy]] [[Arman Cohan]] [[Matthew Peters]]
- Topics: [[nlp_attention]] [[nlp_transformers]] [[nlp_lm]] [[ann_architecture]]
- Venue: #arXiv
- Year: #2020
---
### Techniques
- [[Longformer]] proposes a new [[attention]] mechanism that scales linearly instead of quadratically (normal [[self-attention]])
- Combine #local-windowed-attention with #global-attention
---
### Goal
---
### Major Contributions
- Expands the input sequence lenght of [[BERT]] from 512 to 2048 (4x)
- New attention architectures that do nor grow quadractically
---
### Secondary Contribution
- Long attention spans can be benefitial to long dependency tasks: [[QA]] [[CoRef|Coreference Resolution]] [[document classification]]
---
### Limitations/Future Work
- Improve how attention span works for entire sequences. Do we really need to attent to everything?
- How to better select which spans to attend?
	- Is this task dependent?
- Can we apply [[Longformer]] attention mechanism to other [[Transformers]] based architectures? - as [[RoBERTa]] is quite expensive
---
### Notes (Try to use backlinks)
- Available through #hugging-face API
- Pre-train [[MLM]] continuing from [[RoBERTa]] checkpoint
- Compared systems: [[Transfomer-XL]], [[Reformer]], [[RoBERTa]]
- [[self-attention]] configurations:
	- #full-attention, #sliding-window-attention, #dilated-sliding-window, #global-sliding-window
	- ![[2020_Longformer_attention_types.png]]
	- Positional encoding the same as in [[Transfomer-XL]]
---

