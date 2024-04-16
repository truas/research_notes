### Cross-Document Language Modeling
---
- [Zotero Select Link](zotero://select/groups/2480461/items/7VRRWYUM)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/7VRRWYUM)
- Authors: [[Avi Caciularu]]  [[Matthew Peters]] [[Iz Beltagy]] [[Ido Dagan]]
- Topics: [[nlp_lm]] [[nlp_cdcr]]
- Venue: #arXiv 
- Year: #2021
---
### Major Contributions
- Our cross document language model (CD-LM) improves masked language modeling for these tasks with two key ideas. 
	- First, we pretrain with multiple related documents in a single input, via cross-document masking, which encourages the model to learn cross-document and long-range relationships. 
	- Second, extending the recent [[_2020_Longformer]] model, we pretrain with long contexts of several thousand tokens and introduce a new attention pattern that uses sequence-level global attention to predict masked tokens, while retaining the familiar local attention elsewhere.
- Achieve SOTA in entity crossdocument coreference resolution, paper citation recommendation, and documents plagiarism detection.
---

### Secondary Contribution
---
### Limitations/Future Work
---
### Notes (Try to use backlinks)
- we propose a scheme to integrate cross-document knowledge already in pretraining, thus allowing the LM to learn to encode relevant cross-document relationships implicitly
- This approach considers as input multiple-documents containing related, partly overlapping, information. The model is then challenged to unmask the masked tokens while attending to information in both the same as well as the related documents.
- [[_2019_BERT]] attention heads encode a substantial amount of linguistic knowledge, such as the ability to represent within-document coreference relations.
	- Models dealing with length constraints: [[_2020_Longformer]] [[_2020_Linformer]] [[_2020_BigBird]]
- We hypothesize that the global attention mechanism is useful for learning meaningful representations for modeling cross-document relationships.
	- Global attention can be used to pre-training instead of fine-tuning
- document clusters arereadily available in a variety of existing datasets for cross-document benchmarks, such as summarization (e.g., MultiNews (Fabbri et al., 2019b)), cross-document coreference resolution (e.g., ECB+ (Cybulska and Vossen, 2014b)) and cross-documents alignment benchmarks (Zhou et al., 2020).
- cross-document pretraining strategy directs the model to utilize information across documents for predicting masked tokens, and helps in multiple cross-document down stream tasks.
- Cross-Document Masking In pretraining, we concatenate the document set using new special document separator tokens, and ``<doc-s>`` and ,``<\doc-s>``, for marking document boundaries.
- CD-MLM has a new pretrained special document separator, and pretrained sets of both global and local attention weights that form the cross-document language model
- we employ the Longformer-base model (Beltagy et al., 2020) and continue its pretraining for additional 25k steps.
- Training details
	- Input sequences are of the length of 4,096, effective batch size of 64 (using gradient accumulation and batch size of 8), a maximum learning rate of 3e-5, and a linear warmup of 500 steps, followed by a power 3 polynomial decay. For speeding up the training and reducing memory consumption, we used the mixed precision (16-bits) training mode. The rest of the hyperparameters are the same as for RoBERTa (Liu et al., 2019).
- Coreference Metrics: MUC, B3, CEAFe, their average CoNLL F1, and the more recent LEA metric
- RAND CD-LM is inferior to the plain LONGFORMER model, despite the fact that it already has pretrained document separator embeddings. This emphasizes the requirement of pretraining on related documents rather than random ones, which allows better alignment and paraphrasing capabilities, required for coreference detection.
- ![[2021_CD_LM_train_example.png]]

	
	
	
---
