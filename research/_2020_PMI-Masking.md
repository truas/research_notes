### PMI Masking - Principled Masking of Correlated Spans
---
- [Zotero Select Link](zotero://select/groups/2480461/items/GSIEJE9X)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/GSIEJE9X)
- Authors: [[Yoav Levine]] [[Yoav Shoham]]
- Topics: [[nlp_lm]] [[nlp_transformers]] [[nlp_mlm]]
- Venue: #arXiv
- Year: #2021
---
### Major Contributions
- PMI-Masking, a principled masking strategy based on the concept of Pointwise Mutual Information (PMI)
- more practical approach is to leave the vocabulary as is, but jointly mask co-located words, with the intention of cutting off local statistical “shortcuts” and allowing the model to improve further by learning from broader context
---
### Secondary Contribution
- PMI-masking as an alternative with several advantages: 
	- (i) It is a principled approach, based on a nuanced extension of binary PMI to the n-ary case. 
	- (ii) It leads to better downstream performance,
---
### Limitations/Future Work
---
### Notes (Try to use backlinks)
- The advantage of Whole-Word Masking over Random-Token Masking is relatively modest for standard vocabularies, because out-of-vocabulary words are rare
- Our experiment sought to assess the performance gain obtained from
always masking whole words as opposed to masking each individual token uniformly at random. We compared performance across a range of vocabulary sizes, using the same WordPiece Tokenizer that produced the original vocabulary of 30K tokens. As we decreased a 30K-token vocabulary 10K and 2K tokens, the average length of a word over the pretraining corpus increased from 1.08 to 1.22 and 2.06 tokens respectively. 
---
