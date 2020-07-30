### ELECTRA: Pre-training Text Encoders as Discriminators Rather Than Generators

---
- [Zotero Select Link](zotero://select/groups/2480461/items/QLQEHE2U)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/QLQEHE2U)
- Author: [[Kevin Clark]] [[Christopher Manning]] [[Quoc Le]]
- Topics: [[nlp_transformers]] [[nlp_lm]]
- Venue: #ICLR
- Year: #2020
---

### Techniques
- Drop the [[NSP|Next Sentence Prediction]] but keep [[MLM|Masked Language Model]]
- New training task replaced token detection
- Masked tokens are corrupted by contrastive examples
	- #generator #discriminator architecture
-
---
### Goal
- Improve training architectures from previous [[Transformers]] such as [[BERT]]
	- The [[MLM]] task is not taking advantage of the masked tokens properly
---
### Major Contributions
- [[generator]]  - learns to prodict the original identities of the masked-out tokens
- [[discriminator]] - trained to distinguish tokens in the data from tokens that have been replaced by [[generator]] samples.
---
### Secondary Contribution
- more efficient when using a small [[generator]] and sharing only the embeddings (token and positional) between [[generator]] and [[discriminator]]
	- 1/4-1/2 the size of the [[discriminator]]
- the use of contrastive learning during training
---
### Limitations/Future Work
- The superiorty of [[ELECTRA]] is not that clear (maybe the fact it uses more data has more weight). #GLUE results have several close results with [[AlBERT]] and [[RoBERTa]]
- 
---
### Notes (Try to use backlinks)
- [[ELECTRA]] stands for Efficiently Learning an Encoder that Classifies Token Replacements Accurately
- ![[2020_ELECTRA_architecture.png]]
- [[generator]] is trained with maximum likelihood instead of [[GAN|Generative Adversarial Network]]
- Tasks: #GLUE, #SQuAD , #CoLA, #QQP, #SST, #STS
- Appendix has a full description of hyperparameters and benchmarks used. In special appendix  H brings ideas that did not work out.
---
