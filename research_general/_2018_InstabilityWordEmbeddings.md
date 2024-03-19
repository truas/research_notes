### Factors Influencing the Surprising Instability of Word Embeddings
---
- [Zotero Select Link](zotero://select/groups/2480461/items/ZE6KNFCC)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/ZE6KNFCC)
- Authors: [[Laura Wendlandt]] [[lRada Mihalcea]]
- Topics: [[nlp_embeddings]] [[nlp_instability]]
- Venue: #NAACL
- Year: #2018
---
### Major Contributions
- Explore the limitations of word embeddings wrt properties of the data, algorithm, and words which affect downstream tasks
	- They explore [[_2013_Word2vec]] [[_2014_GloVe]] and [[_2007_PMI]]

---
### Secondary Contribution
- Ridge regression regularizes the magnitude of the model weights, producing a more interpretable model than non-regularized linear regression. This regularization mitigates the effects of multicollinearity (when two features are highly correlated).
- Overall, GloVe is the most stable embedding algorithm. This is particularly apparent when only in-domain data is considered, as in Figure 5. PPMI achieves similar stability, while word2vec lags considerably behind.
---
### Limitations/Future Work
- The donwstream evaluation is poor designed and weak
---
### Notes (Try to use backlinks)
- Use the overlap (%) between nearest neighbors in embedding space as a measure of instability (Why)
	- The same measure used in [[_2018_StabilityWordEmbeddings]]
	- 100% stability indicates perfect agreement between the two embedding spaces, while 0% stability indicates complete disagreement
- we build a regression model that aims to predict the stability of a word given: (1) properties related to the word itself; (2) properties of the data used to train the embeddings; and (3) properties of the algorithm used to construct these embeddings.
	- To make our regression model symmetric, we effectively encode three features: the higher raw frequency (between the two), the lower raw frequency, and the absolute difference in raw frequency.
- The behavior we see here agrees with the conclusion of (Mimno and Thompson, 2017), who find that [[_2014_GloVe]] exhibits more well-behaved geometry than [[_2013_Word2vec]]
---
