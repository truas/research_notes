### End-to-End Training of Neural Retrievers for Open-Domain Question Answering
---
- [Zotero Select Link](zotero://select/groups/2480461/items/S5XYT8TZ)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/S5XYT8TZ)
- Authors: [[Devendra Singh Sachan]] [[Bryan Catanzaro]]
- Topics: [[nlp_qa]] [[nlp_transformers]] [[nlp_task]]
- Venue: #arXiv 
- Year: #2021
---
### Major Contributions
 - an approach of unsupervised pre-training with the Inverse Cloze Task and masked salient spans, followed by supervised finetuning using question-context pairs
 - Two approaches for end-to-end training: the reader considers each retrieved  document separately while in the second approach, the reader considers all the retrieved documents together.
	 - Individual top-k
	 - Joint top-k
---
### Secondary Contribution
- pre-training with masked salient spans is a more effective approach than[[ICT]] when the training dataset sizes are relatively smaller.
---
### Limitations/Future Work
---
### Notes (Try to use backlinks)
- OpenQA
	- In the first stage, given a question, a retriever module identifies the most relevant documents
	- second stage, these relevant documents are given as input to the reader module, which understands them and extracts the answer for the question
- The main drawback of using the BM25 approach for the retriever is that it is not trainable and hence can’t be adapted to different open-retrieval tasks or datasets
- dual-encoder - question and context encoder
- Unsupervised training using [[ICT|Inverse Cloze Task]] and [[Masked salient spans generatie training]]
- We observe that unsupervised training with ICT is quite effective in providing a non-trivial zero-shot retrieval accuracy on both the datasets.
- we showcase that our proposed approach of unsupervised pre-training with both [[ICT]] and masked salient spans followed by supervised finetuning provides improvements of 2-3 points over the strong results that were achieved with supervised training.
- There is also an emerging line of work on performing OpenQA using the knowledge stored in the parameters of a large pre-trained language model (Petroni et al., 2019; Jiang et al., 2020). 
- Impressive performance has been shown for both zero-shot OpenQA (Brown et al., 2020) and when using a small amount of data to finetune the language model (Roberts et al., 2020).
---
