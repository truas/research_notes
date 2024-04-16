### Adapting BERT forWord Sense Disambiguation with Gloss Selection Objective and Example Sentences
---
- [Zotero Select Link](zotero://select/groups/2480461/items/2DM44UED)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/2DM44UED)
- Authors: [[Boon Penn Yap]] [[Eng Siong Chng]]
- Topics: [[nlp_wsd]] [[nlp_transformers]]
- Venue: #EMNLP
- Year: #2020
---
### Major Contributions
- we propose to formulate word sense disambiguation as a relevance ranking task, and fine-tune BERT on sequence-pair ranking task to select the most probable sense definition given a context sentence and a list of candidate sense definitions
- In this paper, we use similar context-gloss pairs as inputs for our proposed WSD model. However, instead of treating individual context-gloss pair as independent training instance, we group related context-gloss pairs as 1 training instance, i.e. context-gloss pairs with the same context but differentcandidate glosses are considered as 1 group.
---
### Secondary Contribution
- It is worth noting that Du et al. (2019) and Huang et al. (2019) reported slightly worse or identical results when fine tuning on BERTlarge, but both of our models fine tuned on BERTlarge obtain considerable better results than the BERTbase counterparts. This may be partially attributed to the fact that we were using the recently released whole-word masking variant of BERTlarge, which was shown to have a better performance on the Multi-Genre Natural Language Inference (MultiNLI) benchmark
---
### Limitations/Future Work
---
### Notes (Try to use backlinks)
- ![[2020_BERT_WSD_Gloss_example.png]]
- The same as our approach for LGMC
---
