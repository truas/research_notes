### How Can We Accelerate Progress Towards Human-like Linguistic Generalization?
---
- [Zotero Select Link](zotero://select/groups/2480461/items/9GPVUQ8Q)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/9GPVUQ8Q)
- Authors: [[Tal Linzen]]
- Topics: [[nlp]] [[nlp_generalization]]
- Venue: #ACL 
- Year: #2020
---
### Major Contributions
- Describe and critique the [[PAID|Pretraining-Agnostic Identically Distributed]] that currently reigns over [[nlp]]:
	- Pretrain of word prediction model [[LM]] on a large corpus
	- Fine-tune [[nlp_transfer_learning]] on training set representing a classification task
	- Evaluation on a test set draw from the same distribution as that training set
- Suggestions of design decisions that can make things more "comparable"/"standard"
	- Standard, moderately sized pretraining corpora
	- Independent evaluation in multiple languages
	- What about grounding? (text alone is not enough - as humans learn)
	- Normative evaluation (test should not be derived from training, instead by expert-created controllled datasets) -> OK, but how do you scale this? Annotation suffers from this problem a lot.
	- Test-only benchmarks
	- What about efficiency
	- Breakdown by task and phenomenon - _we should insist, when reviewing papers, that authors include a complete breakdown by phenomenon as an appendix, and discuss noteworthy patterns in the results._
---
### Secondary Contribution
---
### Limitations/Future Work
---
### Notes (Try to use backlinks)
- Nice discussion about the non-standard pretraining datasets (size):
	- [[_2019_BERT]] -  trained on 3.3 billion words;
	- [[_2019_XLNet]] - trained on 78 GB of text, or approximately 13 billion words;
	- [[_2019_RoBERTa]] - trained on 160 GB of text, or around 28 billion words;
	- [[_2019_T5]] - 750 GB of text, or approximately 130 billion words.
---
