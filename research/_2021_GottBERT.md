### GottBERT: a pure German Language Model

---
- [Zotero Select Link](zotero://select/groups/2480461/items/GR4Q89UW)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/GR4Q89UW)
- Authors: [[Raphael Scheible]] [[Martin Boeker]]
- Topics: [[nlp_transformers]] [[nlp_lm]] [[nlp_low_res_lang]]
- Venue: #arXiv 
- Year: #2021
---
### Major Contributions
- [[_2021_GottBERT]] German BERT model trained from scratch using [[_2020_RoBERTa]] architecture.
---
### Secondary Contribution
- [[_2021_GottBERT]]  is the first published RoBERTa model pre-trained on TPUs.
- [[_2021_GottBERT]] was tested in the German part of CoNLL 2003 and the GermEval 2014 (NER); and GermEval task 2018 (Document Classification)
- 
---
### Limitations/Future Work
- The score is the best of 10 runs of the respective experiment of each trainedmodel. The best score selection is based on validation set.
	- They should have reported the average.
- [[_2021_GottBERT]] used 145GB for its training, raising some concerns about their findings. What brought more benefits, their approach or simpley more data? A training from scratch
---
### Notes (Try to use backlinks)
- no German single language RoBERTa model is yet published, which we introduce in this work (GottBERT).
- Single language models trained with the Open Super-large Crawled ALMAnaCH coRpus (OSCAR) (Ortiz Su´arez et al., 2020) showed good performance due to the size and variance of the [[OSCAR]] (Martin et al., 2020; Delobelle et al., 2020).
- BERT models though, were first released as single language models in English based on 16GB of raw text and as the multilingual model mBERT based on Wikipedia dumps in about 100 languages.
- German BERT was trained using 12GB of raw text data basing on German Wikipedia (6GB), the OpenLegalData dump (2.4GB) and news articles (3.6GB). dbmz BERT used as source data a GermanWikipedia dump, EU Bookshop corpus, Open Subtitles, CommonCrawl, ParaCrawl and News Crawl which sums up to adataset of 16GB.
- The German data portion of the OSCAR measures 145GB of text containing approximately 21.5 billion words in approximately 459 million documents (one document per line).

---
