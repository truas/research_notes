### Unified Language Model Pre-training for Natural Language Understanding and Generation
---
- [Zotero Select Link](zotero://select/groups/2480461/items/VLD3UUNR)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/VLD3UUNR)
- Author: [[Li Dong]] [[Hsiao-Wuen Hon]]
- Topics: [[language_models]] [[topic2]]
- Venue: #arXiv 
- Year: #2019
---
### Goal

To create a unified language model(training) that is capable to perform NLU and NLG.

---

### Major Contributions
- Optimize a transformer network with three training objectives 
	- Bidirectional encoding 
	- Unidirectional decoding
	- Unidirectional decoding conditioned on bidirectional encoding

![[2019_UniLM_training_types.png]]

---
### Secondary Contribution

---
### Limitations/Future Work
---
### Notes (Try to use backlinks)
- Uses [[MASK]] tokens for training like BERT.
- Main three advantages:
	- No need to train multiple LMs to perform NLU and NLG
	- More general representations due to training of multiple objectives and resulting less [[overfitting]] to specific tasks
	- UniLM can perform NLU and NLG at the same time
- Good performance for abstractive summarization, Q&A, response generation.

---
