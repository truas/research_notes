### Kformer: Knowledge Injection in Transformer Feed-Forward Layers
---
- [Zotero Select Link](zotero://select/groups/2480461/items/8Q2XM6AA)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/8Q2XM6AA)
- Authors: [[Yunzhi Yao]] [[Huajun Chen]] 
- Topics: [[nlp_transfer_learning]] [[nlp_knowlegde_representation]]
- Venue: #arXiv #microsoft
- Year: #2022
---
### Major Contributions
- we explore the FFN in Transformer and propose a novel knowledge fusion model, namely Kformer, which incorporates external knowledge through the feed-forward layer in Transformer
	- Kformer contains three main components: firstly for each question, we retrieve the top N potential knowledge from knowledge bases (§3.1).Then, we obtain the knowledge representation via Knowledge Embedding (§3.2). In the end, we fuse the N retrieved knowledge into the pre-trained model via the feed-forward layer in Transformer (§3.3).
- 
---
### Secondary Contribution
---
### Limitations/Future Work
---
### Notes (Try to use backlinks)
- To incorporate external knowledge into language models, previous work mainly integrates the external knowledge on the input level, or the representation level. For the fusion on the input text, the model concatenates the question text and the knowledge together as the input 
- We follow [Dai et al., 2021] and claim that FFN bear high knowledge intensity and store Factual Knowledge and we can inject knowledge into FFN
- Injection method via concatenation (RoBERTa+Concat) and Attention (RoBERTa+ATT)
- As compared to other methods of incorporating information into the model, our model has a distinct benefit. On the test set, our model outperforms the RoBERTa+MCQueen by 0.68. 
- Incorporating the knowledge through self-attention improves very little while injecting via FFN show great improvement. These findings show that FFN can make better use of the injected knowledge than attention.
- Kformer, the layer where we incorporate external knowledge is a critical hyper-parameter since different levels in Transformer may catch different information.
- On both tasks, the model that integrates evidence through the top three layers or the bottom three layers benefits from external knowledge, whereas applying knowledge into the model’s 4-6 layers degrades its performance.
- 
- ![[2022_Kformer_arch.png]]
---
