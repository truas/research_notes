### An Attention Free Transformer
---
- [Zotero Select Link](zotero://select/groups/2480461/items/97B6YZK2)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/97B6YZK2)
- Authors: [[Shuangfei Zhai]] [[Josh Susskind]]
- Topics: [[nlp_transformers]] [[nlp_ann]] [[nlp_attention]] [[ann_architecture]]
- Venue: #arXiv 
- Year: #2021
---
### Major Contributions
- We introduce Attention Free Transformer (AFT), an efficient variant of Transformers that eliminates the need for dot product self attention.
	- AFT is composed of the interaction of three quantities, namely the query, key and value ). The difference is that, in AFT the key and value (context) are first combined 
- We also introduce AFT-local and AFT-conv, two model variants that take advantage of the idea of locality and spatial weight sharing while maintaining global connectivity.
	- We show that the locality constraint not only provides better parameter and computational efficiency, but also greatly improves model’s performance in all tasks.
---
### Secondary Contribution
- Their related work point to interesting contributions in making the transformer architecture more efficient:
	- Approximating the dot product, Sparse/Local  attention, Context compression, eliminating dot product attention, MLP for vision,
---
### Limitations/Future Work
---
### Notes (Try to use backlinks)
- Transformers require high computational costs. The cause of this challenge is the need to perform attention operations that have quadratic time and space complexity w.r.t. the context size. This makes it difficult for Transformers to scale to inputs with large context sizes.
- AFT combines and in an element-wise fashion, while k and v all the linear attention papers rely on matrix dot products.
- AFT-local. In many applications, locality is an important inductive bias, which has been exploited by CNNs and recent works in Transformers [4, 7]. In addition, we found that trained standard Transformers tend to demonstrate extensive local attention patterns. To be concrete, we visualized anImagenetNet pretrained Vision Transformer (ViT) [5], which consists of 12 layers each with 6 heads
	- The goal (hypothesis) is to obtain this sharpness from the left in their AFT approach. Since in the vanilla(conv) version this does not happened, they introduced this locality bias to approximate AFT to AFT-local.
	- ![[2021_AFT_goal.png]]
---
