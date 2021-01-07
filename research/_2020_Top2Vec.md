### Top2Vec: Distributed Representations of Topics
---
- [Zotero Select Link](zotero://select/groups/2480461/items/W23CW6WH)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/W23CW6WH)
- Authors: [[Dimo Angelov]]
- Topics: [[nlp_embeddings]] [[nlp_topic_modeling]]
- Venue: #arXiv
- Year: #2020
---
### Major Contributions
- In the jointly embedded document and word semantic space, a dense area of documents can be interpreted as many documents that have a similar topic. We use this assumption to propose top2vec, a distributed topic vector which is calculated from dense areas of document vectors. 
	- The number of dense areas of documents found in the semantic space is assumed to be the number of prominent topics.
- The top2vec model produces jointly embedded topic, document, and word vectors such that distance between them top2vec represents semantic similarity.
---
### Secondary Contribution
---
### Limitations/Future Work
- LDA and PLSA discretize the continuous topic space into t topics and model documents as mixtures of those t topics.
- The discretization of topics is necessary to model the relationship between documents and words. This is one of the greatest weakness of these models, as the number of topics t or the way to estimate it is rarely known, especially for very large or unfamiliar datasets
- LDA and PLSA use bag-of-words (BOW) representations of documents as input which ignore word semantics

---
### Notes (Try to use backlinks)
- Although word2vec implicitly factorizes a word-context PMI matrix, what it explicitly does is maximize the dot product between word vectors for words which co-occur while minimizing dot product between words which do not co-occur
	- Each word vector in this matrix alone has no meaning; it only gives relative similarity to other word vectors in the matrix
- [[_2003_LDA]] and PLSA model topics as distributions of words, which are used to recreate the original document word distributions with minimal error.
- top2vec topic vector in the semantic embedding represents a prominent topic shared among documents. 
	- The nearest words to a topic vector best describe the topic and its surrounding documents.
- We found that t-SNE does not preserve global structure as well as UMAP and it does not scale well to large datasets
- Common words appear in most documents and, as such, they are often in a region of the semantic space that is equally distant from all documents. As a result the words closest to a topic vector will rarely be stop-words
---
