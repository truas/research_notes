### XLNet: Generalized Autoregressive Pretraining for Language Understanding	

---
- [Zotero Select Link](zotero://select/groups/2480461/items/L9ZYJEYY)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/L9ZYJEYY)
- Author: [[Zhilin Yang]], [[Quoc V. Le]]
- Topics: [[NLT_LM_autoregressive]]
- Venue: #arXiv 
- Year: #2019
---

---
### Goal
- To Overcome issues from independent and parallel Mask token prediction in BERT with a bidirectional autoregressive approach.
---

### Major Contributions
- Instead of using a fixed forward of backward modeling like [[GPT]], XLNet maximizes the expected log-likelihood of a sequence w.r.t. all possible permutations of the tokens to be predicted.
- Therefore, XLNet overcomes the independence assumption of BERT
- XLNet does not use MASK tokens and data corruption to avoid the pretrain-finetune discrepancy.
---

### Secondary Contribution
- Observation: [[NSP]] is unnecessary in the experiments and does not improve anything.
---

### Limitations/Future Work
---

### Notes (Try to use backlinks)
- [[Autoregressive]] vs [[Autoencoding]]:
	- [[Autoregressive]] models the probability of tokens in one direction (e.g. forward or backward)
	- [[Autoencoding]] tries to reconstruct the original data from a corrupted input (e.g., masked sequence)
- The paper claims that there is a pretrain-finetune discrepancy by inserting frequently MASK tokens in pre-training which are never seen in regular text.
- BERT is not able to model the joint probability of masked tokens as they are predicted in parallel. BERT assumes that tokens are independent of each other, which is oversimplified for many cases.
- Uses relative positional encoding and segment recurrence mechanism of [[_2019_Transformer-XL]].
- For explicit reasoning tasks like SQuAD and RACE that involve longer context, the performance gain of XLNet is usually larger. This superiority at dealing with longer context could come from the Transformer-XL backbone in XLNet.
- For classification tasks that already have abundant supervised examples such as MNLI (>390K), Yelp (>560K) and Amazon (>3M), XLNet still lead to substantial gains.
---
