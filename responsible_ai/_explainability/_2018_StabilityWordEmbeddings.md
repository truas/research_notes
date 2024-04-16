### Evaluating the Stability of Embedding-basedWord Similarities
---
- [Zotero Select Link](zotero://select/groups/2480461/items/5W98NKWH)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/5W98NKWH)
- Authors: [[Maria Antoniak]] [[David Mimno]]
- Topics: [[nlp_embeddings]] [[nlp_word_sim]] [[nlp_instability]]
- Venue: #TACL
- Year: #2018
---
### Major Contributions
 - We recommend that users never rely on single embedding models for distance calculations, but rather average over multiple bootstrap samples, especially for small corpora.
	 - Corpus variation focused
 - Goal is to identify the factors that create instability and measure our statistical confidence in the cosine similarities between embeddings trained on small, specific corpora
 - We focus on the training corpus as a source of variation, viewing it as a fragile artifact curated by often arbitrary decisions.
	 -  We examine four different algorithms and six datasets, and we manipulate the corpus by shuffling the order of the documents and taking bootstrap samples of the documents. 
	 -  Finally, we examine the effects of these manipulations on the cosine similarities between embeddings.
 -  We find that there is considerable variability in embeddings that may not be obvious to users of these methods
 -  
---
### Secondary Contribution
- we train 50 LSA models, 50 SGNS models, 50 GloVe models, and 50 PPMI models for each of the three settings (FIXED, SHUFFLED, and BOOTSTRAP), for each document segmentation size, for each corpus
---
### Limitations/Future Work
---
### Notes (Try to use backlinks)
- We find that nearest-neighbor distances are highly sensitive to small changes in the training corpus for a variety of algorithms.
- standard methods dramatically under-represent the variability of these measurements
	- If users  do not account for this variability, their conclusions are likely to be invalid.
- the corpus-centered approach is based on direct human analysis of nearest neighbors to embedding vectors, and the training corpus is not simply an off-the-shelf convenience but rather the central object of study.
	- ![[2018_StabilityWE_DownstreamTask.png]]
- small corpora are common in digital humanities and computational social science, and it is often impossible to mitigate these problems simply by expanding the corpus.
- Corpus order and presence of documents
	- FIXED setting includes each document exactly once, and the documents appear in a constant, chronological order across all models.
	- SHUFFLED setting includes each document exactly once, but the order of the documents is randomized for each model
	- BOOTSTRAP setting samples documents randomly N with replacement, where is equal to the number N of documents in the FIXED setting
- BOOTSTRAP setting causes large increases in variation across all algorithms (with a weaker effect for PPMI) and corpora, with large standard deviations across word rankings.
- As expected, each algorithm has a small variation in the FIXED setting
- We observe that the FIXED and SHUFFLED settings for GloVe and LSA produce the least variable cosine similarities, while PPMI produces the most variable cosine similarities for all settings.
- documents segmented at a more fine-grained level produce embeddings with less variability across runs of the BOOTSTRAP setting. Documents segmented at the sentence level have standard deviations clustering closer to the median, while larger documents have standard deviations that are spread more widely
---
