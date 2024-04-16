### ALBERT: A Lite BERT for Self-supervised Learning of Language Representations

---
- [Zotero Select Link](zotero://select/groups/2480461/items/YUQIX8F3)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/YUQIX8F3)
- Author: [[Zhenzhong Lan]] [[Radu Soricut]]
- Topics: [[nlp_transformers]] [[#distillation]] [[train_arc]] [[SOP]]
- Venue: #ICLR
- Year: #2019 #2020
---
### Techniques
- Modification of [[2019_BERT]]. 
 - Factorized embedding parameterization. Decompose the vocabulary embedding matrix into two small matrices. This splits the size of hidden layers and embeddings (vocabulary)
 - Cross-Layer parameter sharing. Prevents the parameters to grow with the depth of the network
 - [[SOP|Sentece Order Prediction]] Focuses on inter-sentece coherence. This new training architetecture come to solve the inefficiency of  [[NSP]] from [[2019_BERT]]
---
### Goal
---
### Major Contributions
 - This paper proposes three modifications of [[2019_BERT]] type models two of which is concerned with parameter sharing and one with a new auxiliary loss. 
- [[_2019_ALBERT]] is 1.7x faster and has 18x fewer parameters than [[2019_BERT]] large
---
### Secondary Contribution
-  Cross-Layer parameter sharing get better performance on language modeling and subject-verb agreement than the vanilla [[Transformers]]
-  The [[SOP]] work at textual segments rather then sentences. This imposes a harder task than [[NSP]]  - and more useful for some NLP tasks 
-  They argue [[NSP]] is inefficient because its conglates #topic_prediction and #coherence_prediction in a single task
---
### Limitations/Future Work
- inferiror results than [[2019_BERT]] - fewer parameters and processing time
- does the cross-layer parameter sharing (share all parameters across all layers) can lead to overfit?
	- Their empirical results say it does not. After 1M steps training is nor overfit
- 12/24 layers present almost no differente in their results
---
### Notes (Try to use backlinks)
- Interest common quesiton in the paper: Is having better NLP models as easy as having larger models?
- Tasks: #GLUE, #SQuAD , #RACE
- Use [[GELU]] non-linearity
- WordPiece embeddings are meant to learn context-independent representations
- Hidden-layer embeddings are meant to learn context-dependent representations
- L2 distances and cosine similarity show [[_2019_ALBERT]] embeddings are oscillating, rather than converging
	- transitions from layer to layer in are smoother in [[_2019_ALBERT]]
---
