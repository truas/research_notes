### RoBERTa: A Robustly Optimized BERT Pretraining Approach 
---
- [Zotero Select Link](zotero://select/groups/2480461/items/APYKG3XT)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/APYKG3XT)
- Authors: [[Yinhan Liu]] [[Veselin Stoyanov]] [[Omer Levy]]
- Topics: [[nlp_transformers]] [[nlp_lm]]
- Venue: #arXiv 
- Year: #2019
---
### Techniques
- [[_2018_BERT]]
---
### Major Contributions
- Replicate, simplify, and better training tune of [[_2018_BERT]]
- Hyperparameter adjustments to [[_2018_BERT]]
- Longer training with big batches
- Removal of [[NSP]] from [[_2018_BERT]]
- Training of longer sequences
- Dynamically changing the masking pattern applied to the training data instead of the fixed used in [[_2018_BERT]]
---
### Secondary Contribution
- Using individual sentences hurs performance on downstream tasks
	- They have a hypothesis that the model is not able to learn long-range dependencies
- Removing [[NSP]] slightly improves downstream tasks performance
- Throughly investigation of data size and number of training passes through the data
- Large batch training can improve trainin efficiency even without large scale parallel hardware
- Longest-trained model does not appear to overfit their data
---
### Limitations/Future Work
- It's not clear how [[_2019_RoBERTa]] would behve with contrastive tasks in NLP
	- Does it generalize well for WSD?
- They use so much more data, that's quite hard to evaluate if their technique is really making the difference or not
	- For example, using the same amount of data, but removing [[NSP]]would harm their model's performance?
---
### Notes (Try to use backlinks)
- RoBERTa stands for: Robustly optimized BERT approach
- [[_2019_BERT]] on [[MLM]]:
	- 15% of input tokens are selected for possible replacement
		- 80% (of the selected) are replaced with [MASK]
		- 10% (of the selected) are left unchanged
		- 10% (of the selected) are replaced by a random sected vocabulary
- Training is sensitive to the Adam epsilon term
- [[_2019_RoBERTa]] is trained in more data than [[_2019_BERT]], 160GB of uncompressed text, composed of #BookCorpus + #Wikipedia (16GB), #CC-News (76GB), #OpenWebText (38GB), and #Stories (31GB)  
- Tasks: #GLUE  #RACE  #SQuAD 
- Each training instance was duplicated 10 times so each sequence is masked in 10 different ways overt the 40 epochs of training.
- Uses the same [[MLM]] that [[_2019_XLNet]] and [[_2019_BERT]] but outperform then
	- ==_TR: Not so sure about this point in their paper, as they tweaked a lot the masking part, including exapanding the training set so all possible masks would take place_==
- Training formats: Segment-pair+NSP, Sentence-pair+NSP, Full-sentences, Doc-sentences
	- Doc-sentences performs slightly better, but Full-sentences is used because of its fixed structure
- [[_2016_BPE|Byte-Pair Encodding]] is used in their text encoding.
- Compared systems: [[_2019_BERT]] [[_2019_XLNet]] [[_2019_MT-DNN]] [[_2019_ERNIE]] (formely ALICE)
- Section 6 has some references for multi-task fine tuning
---
