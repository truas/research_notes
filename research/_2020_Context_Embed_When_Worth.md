### Contextual Embeddings: When Are They Worth It?

---
- [Zotero Select Link](zotero://select/groups/2480461/items/ZEYDNTTB)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/ZEYDNTTB)
- Author: [[Simran Arora]] [[Christopjer Ré]]
- Topics: [[nlp_embeddings]] [[nlp_transformers]]
- Venue: #ACL
- Year: #2020
---

### Techniques
- [[_2019_BERT]]
- [[GloVe]]

---
### Goal
Explore how contextual embeddings (e.g. BERT) compare to classic pre-trained embeddings (e.g. GloVe)

---
### Major Contributions

---
### Secondary Contributions

---
### Limitations/Future Work

---
### Notes
tr: Extracted Annotations (7/10/2020, 5:13:19 PM)

"Surprisingly, we find that both of these simpler baselines can match contextual embeddings on industry-scale data, and often perform within 5 to 10% accuracy (absolute) on benchmark tasks." (Arora et al 2020:1)

"important research problem is to understand when these contextual embeddings add significant value vs. when it is possible to use more efficient representations without significant degradation in performance" (Arora et al 2020:1)

"we find that in highly optimized production tasks at a major technology company, both classic and random embeddings have competitive (or even slightly better!) performance than the contextual embeddings." (Arora et al 2020:1)

"we find in experiments across a range of tasks that the performance of the non-contextual embeddings (GloVe, random) improves rapidly as we increase the amount of training data, often attaining within 5 to 10% accuracy of BERT embeddings when the full training set is used. This suggests that for many tasks these embeddings could likely match BERT given sufficient data, which is precisely what we observe in our experiments with industry-scale data" (Arora et al 2020:1)

"We show on both sentiment analysis and NER tasks that contextual embeddings perform significantly better on more complex, ambiguous, and unseen language, according to proxies for these properties." (Arora et al 2020:2)

"Pretrained contextual embeddings" (Arora et al 2020:2)

"BERT (Devlin et al., 2018) and XLNet (Yang et al., 2019" (Arora et al 2020:2)

"Pretrained non-contextual embeddings" (Arora et al 2020:2)

"GloVe (Pennington et al., 2014), word2vec (Mikolov et al., 2013), and fastText (Mikolov et al., 2018" (Arora et al 2020:2)

"Random embeddings" (Arora et al 2020:2)

"Limsopatham and Collier (2016)" (Arora et al 2020:2)

"GloVe and random embeddings across a range of named entity recognition (NER) (Tjong Kim Sang and De Meulder, 2003), sentiment analysis (Kim, 2014), and natural language understanding (Wang et al., 2019a) tasks" (Arora et al 2020:3)

Train GloVe and Random embeddings in NER, Sent Analysis, (note on p.3)




"we consider 768- dimensional pretrained BERTBASE word embeddings, 300-dimensional publicly available GloVe embeddings, and 800-dimensional random circulant embeddings." (Arora et al 2020:3)

"no fine-tuning)," (Arora et al 2020:3)

"As a result of this improvement, we show in Table 1 that across tasks when the full training set is used, the non-contextual embeddings can often (1) perform within 10% absolute accuracy of the contextual" (Arora et al 2020:3)

"random (R) and GloVe (G) relative to BERT (B) for NER, sentiment analysis (Sent.), and language understanding (GLUE) tasks" (Arora et al 2020:3)

"We observe that non-contextual embeddings can often (1) perform within absolute accuracy of the contex- 10% tual embeddings, and (2) match the performance of contextual embeddings which are trained on 1x-16x less data." (Arora et al 2020:3)

"embeddings, and (2) match the performance of the contextual embeddings trained on 1x-16x less data, while also being orders of magnitude more computationally efficient." (Arora et al 2020:3)

"Complexity of text structure We hypothesize that language with more complex internal structure will be harder for non-contextual embeddings" (Arora et al 2020:4)

"Ambiguity in word usage We hypothesize that non-contextual embeddings will perform poorly in disambiguating words that are used in multiple different ways in the training set." (Arora et al 2020:4)

"We see that in 19 out of 21 cases, the accuracy gap between BERT and random embeddings is larger on the slice of the validation set corresponding to large metric values, validating our hypothesis that contextual embeddings provide important boosts in accuracy on these points." (Arora et al 2020:4)

"ELMo embeddings (Peters et al., 2018) showed that the gap between contextual and non-contextual embeddings narrowed as the amount of training data increased" (Arora et al 2020:5)

"Our work is not the first to study the downstream performance of embeddings which do not require any pretraining. For example, in the context of neural machine translation (NMT) it is well-known that randomly-initialized embeddings can attain strong performance (Wu et al., 2016; Vaswani et al., 2017); the work of Qi et al. (2018) empirically compares the performance of pretrained and randomlyinitialized embeddings across numerous languages and dataset sizes on NMT tasks" (Arora et al 2020:5)

"We showed that these non-contextual embeddings perform surprisingly well relative to the contextual embeddings on tasks with plentiful labeled data and simple language." (Arora et al 2020:5)

"B.1 Additional Experiment Details" (Arora et al 2020:8)

---