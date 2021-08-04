### PEGASUS: Pre-training with Extracted Gap-sentences for Abstractive Summarization
---
- [Zotero Select Link](paste here)
- [Zotero URI](paste here)
- Authors: [[Jingqing Zhang]] [[Peter J. Liu]] [[Mohammad Saleh]]
- Topics: [[nlp_text_generation]] [[nlp_text_summarization]]
- Venue: #arXiv #ICML
- Year: #2020
---
### Major Contributions
- They use a encoder-decoder architecture in their abstractive summarization system
- Their [[MLM]] masks entire sentences to generate them - pre-training objective
	- Namely [[GSG|Gap Sentence Generation]]
---
### Secondary Contribution
- Fine tune model is fast ca. 1000 examples
- Performed human evaluation as well
- 
---
### Limitations/Future Work
- [[_2020_PEGASUS]] is not tested in [[nlp_nlu]], just summarization
---
### Notes (Try to use backlinks)
- Trained on [[C4]] and [[HugNews]] corpus
- Downstream tasks: [[XSum]], [[CNN/DailyMail]], [[MultiNews]], [[GigaWord]], [[arXiv]], [[PubMed]], [[BIGPATENT]], [[RedditTIFU]], [AESLC[]], [[BillSum]]
- Rich downstream  datasets
- base model: 224M (batch 256), large 568M (batch 8192)
- A significant hyper-parameter in [[GSG]] is the [[GSR|gap-sentences ratio ]]. A low GSR makes the pre-training less challenging and computationally efficient
- They compared two tokenization methods [[_2016_BPE]] and [[_2018_Unigram]]
- they found that choosing perplexity-optimized models using aggregated ROUGE (rather than directly optimizing ROUGE as in Paulus et al. (2017)) resulted in qualitatively good models
---
