### Plug and Play Language Models: A Simple Approach to Controlled Text Generation
---
- [Zotero Select Link](zotero://select/groups/2480461/items/YHPCJZZ8)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/YHPCJZZ8)
- Authors: [[Summanth Dathathri]] [[Rosanne Liu]]
- Topics: [[nlp_lm]] [[nlp_text_generation]]
- Venue: #ICLR
- Year: #2020
---
### Major Contributions
- Simple Text-Generation model [[PPLM|Plug and Play Language Model]] for controllend text generation that combines pretrained LM with one or more simple attribute classifieers that guide text generation
	- [[BOW]] for topic; linear dicriminator to control sentiment
- [[PPLM]] is compared with [[_2019_CTRL]] and [[_2019_GPT-2]]
- 
---
### Secondary Contribution
- Good human evaluation for fluency and A/B testing
---
### Limitations/Future Work
---
### Notes (Try to use backlinks)
- Their proposed [[PPLM]] was inspired by the [[PPGN|Plug and Play Generative Networks]] (Nguyen et al 2017) from [[computer vision]]
- performed ex post facto in the activation space, therefore no re-training or finetuning is needed
- [[PPLM]] does not require retraining any conditional generative model, and both the language model and the conditional model can be flexibly assembled
- ![[2020_PPLM_models.png]]
- We note that gradient-based latent updates have significantly greater influence on topic relevance (R with or without C) than reranking based on the score (C with or without R), showing that shifting meaning in latent space is more effective than shifting the output distribution directly through reweighting.
---
