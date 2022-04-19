### Automatic Detection of Generated Text is Easiest when Humans are Fooled
---
- [Zotero Select Link](zotero://select/groups/2480461/items/X6J9RW2Q)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/X6J9RW2Q)
- Authors: [[Daphne Ippolito]] [[Douglas Eck]] 
- Topics: [[nlp_ppd]] [[nlp_ann]] [[nlp_explain]] [[nlp_eval]]
- Venue: #ACL
- Year: #2020
---
### Major Contributions
- we perform careful benchmarking and analysis of three popular sampling-based decoding strategies—topk, nucleus sampling, and untruncated random sampling—and show that improvements in decoding methods have primarily optimized for fooling humans.
	- we study three popular random decoding strategies—**top-k, nucleus, and temperature sampling**—applied to GPT-2 (Radford et al., 2019).
- as the number of unlikely words available to be chosen is increased, humans get better at detecting fakes while automatic systems get worse.
---
### Secondary Contribution
- we further find that classifiers are brittle; they generalize poorly when trained to discriminate samples from one strategy and then evaluated on samples from another.
- we create two datasets, one with no priming, and one with the minimum amount of priming possible: a single token of web text. This means that for every excerpt of web text in the training set, there is an excerpt of machinegenerated text that starts with the same token. We find that even with limited priming, the ability of automatic detectors can be strongly impacted.
- Overall we find that human raters—even “expert” trained ones—have consistently worse accuracy than automatic discriminators for all decoding methods and excerpt lengths. In our experiments, randomly-selected pairs of raters agree with each other on a mere 59% of excerpts on average. (In comparison, raters and discriminators agree on 61% to 70% of excerpts depending on the discriminator considered)
- we find that human raters and discriminators make decisions based on different qualities, with humans more easily noticing semantic errors and discriminators picking up on statistical artifacts
- Really cool way to check for AMT attention: Figure 7: For some of the questions, the text ”Dear AMT Worker: to show you’re reading, please select definitely [X] for this one.” was inserted into the last text segment, and ”Did you read carefully?” was appended to the end.
---
### Limitations/Future Work
- Identifying ways to improve the language models and decoding strategies we use in order to generate text that is both exciting (ie. unlikely) and semantically plausible. 
- Building better world understanding into automatic discriminators so that they are more capable of detecting the types of errors that humans notice. 
- Developing tools and educational materials to improve humans’ ability to detect machine-generated text. These may include automatic detectors with components that explain their predictions.
---
### Notes (Try to use backlinks)
- only subtle logical fallacies or idiosyncrasies of language give away the text as machine-generated, errors that require a close reading and/or domain knowledge for humans to detect.
- there has thus been little inquiry into the textual properties that cause humans to give generated text high human-like ratings compared to those that cause automatic systems to rate it highly.
- Top-k random sampling, where low-likelihood words are restricted from being generated
- automatic systems excel at identifying statistical anomalies and struggle to build deeper semantic understanding. Top-k in particular creates text that is easy for machines to detect but very hard for humans.
- GROVER, in particular, has been shown to generate fake news that is more trustworthy than human-written fake news according to human raters.
- given an excerpt of text, label it as either human-written or machine-generated. In particular, we are interested in how variables such as excerpt length and decoding strategy impact performance on this classification task
- random sampling approach is that these probability distributions often contain a long tail of vocabulary items that are individually low-probability but cumulatively comprise a substantial amount of probability mass. Holtzman et al. (2020) observe that choosing tokens from this tail often leads to incoherent generations.
- **Task** They are first shown an excerpt of length 16 WordPiece tokens. After they make a guess, the length of the excerpt is doubled, and they are asked the same question again. This continues until the entire passage of length 192 tokens is shown.
- Reassuringly, BERT far surpasses all simple baselines, indicating that it is not fully possible to solve the detection problem without complex sequence-based understanding.
- While Gehrmann et al. (2019) report an AUC of 0.87 on classifying text as real or generated using logistic regression on the four buckets of the GLTR system, we report AUC between 0.52 and 0.56 for this task. The discrepancy is likely due to the fact that the human-written text in our discriminator training set comes from the same distribution as the text used to train the language model, while in GLTR the human text comes from children’s books, scientific abstracts, and newspaper articles.
- In fact, See et al. (2019) note that it takes setting k to 1000 to achieve about the same amount of rare word usage and fraction of non-stopword text as as human writing.3 This makes it very easy for the model to pick out machine-generated text based on these distributional differences.
- Only the discriminator trained with nucleus sampling (a compromise between unmodified sampling and top-k) was able to detect sequences from the other sampling strategies without too much of a hit to accuracy
- For both the Amazon Mechanical Turk raters and the expert raters initial predictions were biased towards ‘possibly human,’ and only by observing more tokens did their predictions become more confident. Figure 4 shows that ‘possibly human’ is by far the most frequent answer upon observing 16 tokens, and as more tokens are observed raters gravitate towards ‘definitely human’ or ‘definitely machine.’ Even at 192 tokens, many raters are still uncertain.
---
