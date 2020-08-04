### Add title here
---
- [Zotero Select Link](zotero://select/groups/2480461/items/S6GRXIHC)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/S6GRXIHC)
- Authors: [[Or Sharir]] [[Barak Peleg]]
- Topics: [[nlp_lm]] [[ann_architecture]] [[nlp]] [[ann_cost]] [[nlp_cost ]]
- Venue: #arXiv 
- Year: #2020
---
### Techniques
- [[Transformers]]
---
### Major Contributions
- Compare different [[LM|Language Models]] training with respect to their economic cost in NLP.
- They point some alternatives to tame the expanding costs in NLP training models:
	- Reduction of raw-compute prices from bigholders. Offer and demand. AWS, Google, Microsoft
	- More efficient neural networl architectures. [[_2020_Reformer]] for example propose to change the traditional [[attention]]  mechanisms from quadratic to `O(n log n)`
	- Ending [[SOTA|State-of-the-Art]] race. Leaderboards top positions are getting less attrative if the innovation comes from more data or more processing.
	- Maxing out on useful data. Data has a limit.
	- Useful as NN are, there is a school of thought that holds that statistical [[ML|Machine Learning]] is necessary but not enough. We should think how to incorporate structured knowledge and symbolic methods into our models.
	---
### Secondary Contribution
- Major relevant categories: 
	- size of dataset
	- model size (number of parameters)
	- training volume (tokens processed - sequence length, training steps, batch size)
- [[Transformers]] attributes:
	- Layers
	- Attention heads
	- Contextual-Embedding Dimension
	- Feed-Forward Dimension
---
### Limitations/Future Work
---
### Notes (Try to use backlinks)
- The cost of floating-point operations ([[FLOPs]]), the basic Neural Network (NN) operation, has been decreasing
- Eventhough the cost for training large models is falling the operational overall cost is increasing
- training the 11B variant parameter of T5 cost well above $1.3 million for a single run. Assuming 2-3 runs of the large model and hundreds of the small ones, the (list-)price tag for the entire project may have been $10Mi.
- The reason the community has adopted the mega-scale, brute-force statistical approach is that it works; it has yielded better performance than any alternative.
---
