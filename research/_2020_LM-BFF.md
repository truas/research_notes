### Making Pre-trained Language Models Better Few-shot Learners
---
- [Zotero Select Link](paste here)
- [Zotero URI](paste here)
- Authors: [[Tianyu Gao]] [[Danqi Chen]]
- Topics: [[nlp_lm]] [[nlp_task]]
- Venue: #arXiv 
- Year: #2021
---
### Major Contributions
- We present [[LM-BFF]]—better few-shot fine-tuning of language models - a suite of simple and complementary techniques for fine tuning language models on a small number of annotated examples
	- (1) prompt-based fine-tuning together with a novel pipeline for automating prompt generation;
	- (2) a refined strategy for dynamically and selectively incorporating demonstrations into each context.
---
### Secondary Contribution
---
### Limitations/Future Work
---
### Notes (Try to use backlinks)
- introduce a novel decoding objective to automatically generate prompts given the few-shot training data using the generative T5 model (Raffel et al., 2020).
- we follow the route of prompt-based prediction, first developed by the GPT series (Radfordet al., 2018, 2019; Brown et al., 2020) for zero-shotprediction and recently studied by PET (Schick and Schutze, 2020a,b) for fine-tuning.
- ![[2020_LM-BFF_example.png]]

---
