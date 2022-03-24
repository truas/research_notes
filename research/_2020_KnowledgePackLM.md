### How Much Knowledge Can You Pack Into the Parameters of a Language Model?
---
- [Zotero Select Link](zotero://select/groups/2480461/items/SHSRM8DZ)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/SHSRM8DZ)
- Authors: [[Adam Roberts]] [[Colin Raffel]] [[Noam Shazeer]] 
- Topics: [[nlp_transformers]] [[nlp_lm]] [[nlp_knowlegde_representation]]
- Venue: #ACL 
- Year: #2020
---
### Major Contributions
- “we take a different approach by evaluating the capability of language models on the practical task of opendomain question answering
	- specifically, we finetune the model to answer questions without access to any external knowledge or context. To do so, the model must parse a natural language query and “look up information” stored in its parameters” (Roberts et al., 2020, p. 5418)
	- “A separate question we address in this work is whether models with more parameters end up storing more information.” (Roberts et al., 2020, p. 5419)
	- 
---
### Secondary Contribution
- [link](https://github.com/google-research/google-research/tree/master/t5_closed_book_qa)
- 
---
### Limitations/Future Work
- “our model distributes knowledge in its parameters in an inexplicable way and hallucinates realistic-looking answers when it is unsure.
- the maximum-likelihood objective used to train our model provides no guarantees as to whether a model will learn a fact or not. This makes it difficult to ensure that the model obtains specific knowledge over the course of pre-training and prevents us from explicitly updating or removing knowledge from a pre-trained model. 
- Finally, the tasks we used in this paper mainly measure “trivia”-style knowledge.” (Roberts et al., 2020, p. 5422)
---
### Notes (Try to use backlinks)
- “we consider open-domain question answering with the additional constraint that the model is not allowed to access any external knowledge whatsoever when answering questions” (Roberts et al., 2020, p. 5419)
- “In question answering in particular, most state-ofthe-art systems use some form of transfer learning.” (Roberts et al., 2020, p. 5419)
- “Encoder-only models are not applicable to closed-book question answering because no context is provided to extract the answer span from” (Roberts et al., 2020, p. 5419)
- Training - “Training We leverage the pre-trained models provided by Raffel et al. (2019), referred to as the “Text-to-Text Transfer Transformer” (T5). The original T5 models were pre-trained on a multitask mixture including an unsupervised “span corruption” task on the C4 dataset as well as supervised translation, summarization, classification, and reading comprehension tasks.” (Roberts et al., 2020, p. 5420)
- “Salient Span Masking Recently, Guu et al. (2020) found that a “salient span masking” (SSM) pre-training objective produced substantially better results in open-domain question answering” (Roberts et al., 2020, p. 5421)
- “we have shown that large language models pre-trained on unstructured text can attain competitive results on open-domain question answering benchmarks without any access to external knowledge. This suggests a fundamentally different approach to designing question answering systems, motivating many threads for future work:” (Roberts et al., 2020, p. 5422)
- ““open-book” models typically provide some indication of what information they accessed when answering a question. This can provide a useful form of interpretability. In contrast, our model distributes knowledge in its parameters in an inexplicable way and hallucinates realistic-looking answers when it is unsure.” (Roberts et al., 2020, p. 5422)
---
