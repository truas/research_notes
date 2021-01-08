### Pre-training is a Hot Topic: Contextualized Document Embeddings Improve Topic Coherence
---
- [Zotero Select Link](paste here)
- [Zotero URI](paste here)
- Authors: [[Frederico Bianci]] [[Dirk Hovy]]
- Topics: [[nlp_embeddings]] [[nlp_transformers]] [[nlp_topic_modeling]]
- Venue: #arXiv
- Year: #2020
---
### Major Contributions
- we extend ProdLDA (Srivastava and Sutton, 2017), a state-of-the-art topic model that implements black-box variational inference (Ranganath et al., 2014), to include BERT representations.
	- adding contextual information to neural topic models enriches the representations, and provides a significant increase in topic coherence
---
### Secondary Contribution
---
### Limitations/Future Work
- the sentence-length limit of SBERT

---
### Notes (Try to use backlinks)
- Even for neural topic models, there exists little work on incorporating external knowl
edge, e.g., word embeddings (Gupta et al., 2019; Dieng et al., 2019).
- Contextualized Topic Modeling: (i) the neural topic model Neural-ProdLDA (Srivastava and Sutton, 2017) and (ii) the SBERT (Sentence BERT) embedded representations (Reimers and Gurevych, 2019).
- Normalized Pointwise Mutual Information (NPMI) measures how much the top-10 words of a topic are related to each other, considering the empirical frequency of the words computed on the original corpus
- external word embeddings topic coherence: compute the average pairwise cosine similarity of the word embeddings of the top-10 words in a topic — using (Mikolov et al., 2013) embeddings. Then, we compute the overall average of those values for all the topics
- Ranked-biased overlap (RBO) compares two topics of the same model. The key
qualities of this measure are twofold: it allows disjointedness between the lists of topics (i.e., two topics can have different words in them) and it is weighted on the ranking (i.e., two lists that share some of the same words, albeit at different rankings, are penalized less than two lists that share the same words at the highest ranks).
- 
---
