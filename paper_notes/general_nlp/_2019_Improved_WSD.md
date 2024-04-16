### Improved Word Sense Disambiguation Using Pre-Trained Contextualized Word Representations
---
- [Zotero Select Link](zotero://select/groups/2480461/items/ACBH8Y6P)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/ACBH8Y6P)
- Authors: [[Christian Hadiwinoto]] [[Wee Chung Gan]]
- Topics: [[nlp_wsd]] [[nlp_embeddings]] [[nlp_transformers]]
- Venue: #EMNLP 
- Year: #2019
---
### Major Contributions
- they Propose different strategies to incorporate pre-trained contextualized  word representations:
	- Nearest Neighbor Matching between test and training (K=1)
	- Linear projection of hidden layers: perform a linear porjection of the hidden vector h_i by n affine transformation into an output sense vector, with its dimension equal to the number of senses for word x_i
		- Using last layer projection
		- Gated Linear Unit
		- Weighted sum of hiddent layers
---
### Secondary Contribution
---
### Limitations/Future Work
- only use SemEval
- related work does not relate their contribution
- Experiments
---
### Notes (Try to use backlinks)
- Work focus only in [[WSD]] and not how this affects further tasks, such as [[LM]]
- Best approach uses linear projection models, which projects the last hidden layer or the weighted sum of all hidden layers to an output sense vector
	- BERT hidden layer outputs as contextual features, which serve as useful cues in determining the word senses
---
