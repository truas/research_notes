### Improving Neural Topic Models using Knowledge Distillation (BAT)
---
- [Zotero Select Link](zotero://select/groups/2480461/items/Z4M33AEU)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/Z4M33AEU)
- Authors: [[Alexander Hoyle]] [[Philip Resnik]]
- Topics: [[nlp_topic_modeling]] [[nlp_transformers]]
- Venue: #EMNLP 
- Year: #2020
---
### Major Contributions
- BERT based Autoencoder as Teacher (BAT),
	- The BERT autoencoder, as “teacher”, provides a dense prediction that is richly informed by training on a large corpus. The topic model, as “student”, is generating its own prediction of that distribution.
---
### Secondary Contribution
- While distillation usually involves two models of the same type, it can also apply to models of differing architectures.
- our approach is flexible enough to easily accommodate any neural topic model, so long as it includes a word-level document reconstruction objective.
- They use [[_2020_DistilBERT]] as their model.
- 
---
### Limitations/Future Work
- reader familiar with variational NTMs may notice that we haven’t mentioned an obvious means of incorporating representations from a pretrained transformer: encoding the document representation from a BERT-like model. This yields unimpressive results; see Appendix D.1
- In future work, we also hope to explore the effects of the pretraining corpus (Gururangan et al., 2020) and teachers (besides BERT) on the generated topics. Another intriguing direction is exploring the connection between our methods and neural network interpretability.
- as the weight on the BERT autoencoder logits goes to one, the topic model begins to describe less the corpus and more the teacher. We believe mining this connection can open up further research avenues; for instance, by investigating the differences in such teacher-topics conditioned on the pre-training corpus
- Explore the power of NTM + Transformers into downstream tasks
---
### Notes (Try to use backlinks)
- NTM (neural topic modeling) surpass LDA
- knowledge distillation (KD, Hinton et al., 2015). The authors argue that the knowledge learned by a large “cumbersome” classifier on extensive data—e.g., a deep neural network or an ensemble—is expressed in its probability estimates over classes, and not just contained in its parameters.
- BAT can apply straightforwardly to other models, be cause it makes very few assumptions about the base model—requiring only that it rely on a word-level reconstruction objective, which is true of the majority of neural topic models proposed to date
- An additional key advantage for our method is that it involves only a slight change to the underlying topic model, rather than the specialized designs by related methods.
---
