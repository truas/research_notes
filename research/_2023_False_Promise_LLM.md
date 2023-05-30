### The False Promise of Imitating Proprietary LLMs
---
- [Zotero Select Link](zotero://select/groups/2480461/items/PGKTZX5S)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/PGKTZX5S)
- Authors: [[Arnav Gudibande]] [[Eric Wallace]]  [[Charlie Snell]] [[Dawn Song]] 
- Topics: [[nlp_LLM]] [[nlp_proprietary]]
- Venue: #arxiv
- Year: #2023

---
### Major Contributions
- when conducting more targeted automatic evaluations, we find that imitation models close little to none of the gap from the base LM to ChatGPT on tasks that are not heavily supported in the imitation data.
---
### Secondary Contribution
- we argue that the highest leverage action for improving open-source models is to tackle the difficult challenge of developing better base LMs, rather than taking the shortcut of imitating proprietary systems.
- Sources of [[ShareGPTMix]] -Interactions
	- ShareGPT: we use approximately 90K dialogues shared by users on the website ShareGPT. To maintain data quality, we deduplicated on the query level and removed any non-English conversations using a language detector. This leaves approximately 50K examples, each of which consist of multiple turns of dialogue.
	- HC3 (Guo et al., 2023): we use the ChatGPT responses from the English Human-ChatGPT Comparison Corpus. This contains ∼27K ChatGPT responses for ∼24K questions. 
	- Discord ChatGPT Bots: we use 10k input-output examples collected from the r/ChatGPT and Turing AI Discord servers, two public channels that allow users to interact with ChatGPT bots.
---
### Limitations/Future Work
- 
---
### Notes (Try to use backlinks)
- open-source LMs are becoming increasingly accurate, with models like LLaMA and FLAN-T5 providing many of the same basic capabilities as their commercial counterparts, albeit at a lower level of performance (Touvron et al., 2023; Chung et al., 2022).
- Our main conclusion is that the biggest limitation of current open-source LMs is their weaker base capabilities.
- In this work, we study one possible resolution to this question: model imitation (Wallace et al., 2020; Orekondy et al., 2019). The premise of model imitation is that once a proprietary LM is made available via API, one can collect a dataset of API outputs and use it to fine-tune an open-source LM. In theory, this imitation process may provide an easy method to distill (Hinton et al., 2014) the capabilities of any proprietary model, thus implying that open-source LMs will always be competitive with their commercial counterparts.
- However, when conducting more targeted automatic evaluations, we found that the imitation models close little to none of the large gap between LLaMA and ChatGPT. In particular, we demonstrate that imitation models improve on evaluation tasks that are heavily supported in the imitation training data
- Proprietary LMs such as ChatGPT consist of two key aspects: proprietary base LMs and proprietary fine-tuning data.
- In model imitation, the goal is to collect data using the API to train an LM that achieves comparable performance to it, i.e., essentially distilling the target LM using an imitation training set (Wallace et al., 2020; Orekondy et al., 2019; Tramer et al., 2016). Potential reasons for performing imitation range from benign to illegal:
	- Academics can use powerful imitation LMs to drive new research projects.
	- Companies can use imitation LMs to launch services that compete with the proprietary system.
	- Malicious users could use imitation models to accelerate progress on nefarious use cases.
- **Broad Imitation**: Broad-coverage imitation is challenging because (1) one must collect an extremely diverse imitation dataset and (2) imitation models must capture this wide data distribution and generalize similarly to the target model on a myriad of held-out examples.
- [[ShareGPTMix]] - There is high diversity in the instructions: for each user query in the dataset, the most similar other user query has an average BLEU score similarity of just 8%. 
	- This is considerably lower than that of other datasets such as SuperNaturalInstructions (Wang et al., 2022b), which is at 61% BLEU similarity for a similarly sized set of examples.
- We found that across every benchmark that we measured, ShareGPT-mix imitation models do not improve (or even decline) in accuracy as compared to the base model, even when adding additional imitation data (Figure 4, top). 
	- he imitation models have weak factuality. In other words, imitation models actually embody some of the worst aspects of AI assistants: their answers sound confident but are less factual than ChatGPT
- We find that imitation models perform well according to human evaluations because they are adept at mimicking ChatGPT’s style—they output fluent, confident, and well-structured answers.
- Finetuning as a simple knowledge extractor. Our results show that a modest amount of finetuning provides little to no improvements on an LM’s knowledge or capabilities. We thus agree with the view that pre-training is the main source of an LM’s capabilities, and that finetuning acts as a lightweight method to train the model to extract its own knowledge Schulman (2023)
- ![[2023_False_Promise_LLM_comparision.png]]
---
