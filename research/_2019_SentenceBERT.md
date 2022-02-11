### Title
---
- [Zotero Select Link](zotero://select/groups/2480461/items/DAUADCZV)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/DAUADCZV)
- Authors: [[Nils Reimers]]  [[Iryna Gurevych]]
- Topics: [[nlp_transformers]] [[nlp_lm]]
- Venue: #EMNLP 
- Year: #2019
---
### Major Contributions
- [SentenceBERT](https://github.com/UKPLab/sentence-transformers)
- we developed SBERT. The siamese network architecture enables that
fixed-sized vectors for input sentences can be derived.
-	Using a similarity measure like cosine similarity or Manhatten / Euclidean distance, se mantically similar sentences can be found. These similarity measures can be performed extremely efficient on modern hardware, allowing SBERT to be used for semantic similarity search as well as for clustering.
- 
---
### Secondary Contribution
- Their Sentence version of [[_2019_BERT]] and [[_2019_RoBERTa]] do perform better than their source versions in the STS tasks.
- Also better than plain GloVe
- SBERT is based on PyTorch. For improved computation of sentence embeddings, we implemented a smart batching strategy: Sentences with similar lengths are grouped together and are only padded to the longest element in a mini-batch. This drastically reduces computational overhead from padding tokens
---
### Limitations/Future Work
---
### Notes (Try to use backlinks)
- we present Sentence-BERT (SBERT), a modification of the pretrained BERT network that use siamese and triplet network structures to derive semantically meaningful sentence embeddings that can be com pared using cosine-similarity.
- sentences into BERT and to derive fixed size sentence embeddings. The most commonly used approach is to average the BERT output layer (known as BERT embeddings) or by using the output of the first token (the token). As we[CLS] will show, this common practice yields rather bad sentence embeddings, often worse than averaging GloVe embeddings (Pennington et al., 2014).
- We fine-tune SBERT on NLI data, which creates sentence embeddings that significantly outperform other state-of-the-art sentence embedding methods like InferSent (Conneau et al., 2017) and Universal Sentence Encoder (Cer et al., 2018).
- SBERT adds a pooling operation to the output of BERT / RoBERTa to derive a fixed sized sentence embedding
	- Using the output of the CLS-token,
	- computing the mean of all output vectors (MEAN strategy) - Default
	- and computing a max-over-time of the output vectors (MAX-strategy). 
- we create siamese and triplet networks (Schroff et al.,2015) to update the weights such that the produced sentence embeddings are semantically meaningful and can be compared with cosine-similarity.
- We experiment with the following structures and objective functions.
	- *Classification Objective Function*. We concatenate the sentence embeddings u and v with the element-wise difference u-v and multiply itwith the trainable weight
	- *Regression Objective Function*. The cosine similarity between the two sentence embeddings and is computed
	- *Triplet Objective Function.* Given an anchor sentence a, a positive sentence p, and a negative p sentence n, triplet loss tunes the network such that the distance between a and p is smaller than the distance between a and n
- The results shows that directly using the output of BERT leads to rather poor performances
	- worse than computing average GloVe embeddings
- The objective function (classification vs. regression) depends on the annotated dataset. 
	- For the classification objective function, we train SBERT base on the SNLI and the Multi-NLI dataset. 
	- For the regression objective function, we train on the training set of the STS benchmark dataset. Perfor mances are measured on the development split of the STS benchmark dataset
	- ![[2019_SentenceBERT_Ablation_Siamese.png]]
---
