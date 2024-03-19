### Improving language models by retrieving from trillions of tokens
---
- [Zotero Select Link](zotero://select/groups/2480461/items/YQXRAFAC)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/YQXRAFAC)
- Authors: [[Sebastian Borgeaud]] [[Arthur Mensch]] [[Jordan Hoffman]] [[Laurent Sifre]]
- Topics: [[nlp_lm]] [[nlp_transformers]] [[deep_mind]]
- Venue: #arXiv
- Year: #2022
---
### Major Contributions
- we suggest retrieval from a large text database as a complementary path to scaling language models. Instead of increasing the size of the model and training on more data, we equip models with the ability to directly access a large database to perform predictions (a semi-parametric approach).
- We introduce [[_2022_RETRO]], a retrieval-enhanced autoregressive language model  We use a chunked cross-attention module to incorporate the retrieved text (§2.4), with time complexity linear in the amount of retrieved data. We show that retrieving based on a pre-trained frozen [[_2019_BERT]] works at scale, removing the need for training and updating a retriever network.
- Our largest model obtains state-of-the-art results on a range of downstream evaluation  datasets including Wikitext103 (Merity et al., 2017) and the Pile (Gao et al., 2020)
- we show that the performance of [[_2022_RETRO]] comes from both explicit neighbour copying and general knowledge extraction.
---
### Secondary Contribution
- [[Retrieval-Enhanced Transformer (Retro)|RETRO]] obtains comparable performance to GPT-3 and Jurassic-1 on the Pile, despite using 25% fewer parameters
---
### Limitations/Future Work
---
### Notes (Try to use backlinks)
 - On large language models - The benefits of increasing the number of parameters come from two factors: additional computations at training and inference time, and increased memorization of the training data
 - To limit test set leakage, we compute the 13-gram Jaccard similarity between train and test documents using the MinHash scheme and remove all training documents with high similarity (0.8 or higher) to a validation or test set document
 - Jurassic-1 (Lieber et al., 2021) show that scaling up language models leads to massive improvements on many downstream tasks
 - Retro models are flexible and can be used without retrieval at evaluation and still achieve comparable performance to baseline models. Conversely, baseline models can be rapidly fine-tuned into Retro models to obtain nearly the same performance as if trained from scratch.
 - ![[2022_RETRO_architecture.png]]
---
