### Learning to summarize from human feedback
---
- [Zotero Select Link](zotero://select/groups/2480461/items/3B8XRAUC)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/3B8XRAUC)
- Authors: [[Nisan Stiennon]] [[Paul Christiano]]
- Topics: [[nlp_text_summarization]]
- Venue: #NIPS
- Year: #2020
---
### Major Contributions
- (1) We show that training with human feedback significantly outperforms very strong baselines on English summarization.
- (2) We show human feedback models generalize much better to new domains than supervised models.
- (3) We conduct extensive empirical analyses of our policy and reward model.
- (4) We publicly release our human feedback dataset for further research
	- The dataset contains 64,832 summary comparisons on the TL;DR dataset,
---
### Secondary Contribution
---
### Limitations/Future Work
- One limitation of our work is the time and cost required to produce our final models. Notably, fine-tuning our 6.7B model with RL required approximately 320 GPU-days.
- We are particularly interested in scaling human feedback to tasks where humans can’t easily evaluate the quality of model outputs. In this setting, it is particularly challenging to identify whether an ML system is aligned with the human designer’s intentions. One approach is to train ML systems to help humans perform the evaluation task quickly and accurately
- Unfortunately, our techniques also enable malicious actors to more easily train models that cause societal harm. For instance, one could use human feedback to fine-tune a language model to be more ersuasive and manipulate humans’ beliefs, or to induce dependence of humans on the technology, or to generate large amounts of toxic or hurtful content intended to harm specific individuals.
---
### Notes (Try to use backlinks)
- summarization models are often trained to predict human reference summaries and
evaluated using ROUGE, but both of these metrics are rough proxies for what we really care about -> summary quality. [sample](https://openaipublic.blob.core.windows.net/summarize-from-feedback/website/index.html#/)
- All of our models are Transformer decoders  in the style of GPT-3 . We conduct our human feedback experiments on models with 1.3 billion (1.3B) and 6.7 billion (6.7B) parameters.
- ![[2020_LearningSummarize_diagram.png]]
- Policies trained with human feedback are preferred to much larger supervised policies
	- Our 6.7B model in turn significantly outperforms our 1.3B model, suggesting that training with human feedback also benefits from scale.
- Controlling for summary length.
- 
---
