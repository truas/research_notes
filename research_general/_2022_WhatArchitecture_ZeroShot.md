### What Language Model Architecture and Pretraining Objective Work Best for Zero-Shot Generalization?
---
- [Zotero Select Link](zotero://select/groups/2480461/items/2N2ZUN8J)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/2N2ZUN8J)
- Authors: [[Thomas Wang]] [[Adam Roberts]] [[Colin Raffel]] 
- Topics: [[nlp_lm]] [[ann_architecture]] 
- Venue: #arXiv 
- Year: #2022 
---
### Major Contributions
- we present a large-scale evaluation of modeling choices and their impact on zero-shot generalization. In particular, we focus on text-to-text models and experiment with three model architectures (causal/non-causal decoder-only and encoder-decoder), trained with two different pretraining objectives (autoregressive and masked language modeling), and evaluated with and without multitask prompted finetuning.
	- Our experiments show that causal decoder-only models trained on an autoregressive language modeling objective exhibit the strongest zero-shot generalization after purely unsupervised pretraining.
- Contributions
	- **Large-scale systematic study.** We undertake a study of architecture and pretraining objective combinations for LLMs with a focus on zero-shot generalization . We consider decoder-only and encoder-decoder models using standard, prefix, and masked language modeling, spanning six 〈architecture, objective〉 pairs. We also evaluate performance with and without multitask finetuning .
	- **Multitask finetuning impacts architecture and objective choice.** We find that the popular recipe of a decoder-only model trained with a standard FLM objective performs best when zero-shot capabilities are measured immediately after pretraining, without any finetuning or adaptation. However, after multitask finetuning, the results are the opposite: models pretrained with MLM perform significantly better and decoder-only models perform worse.
	- **Bridging across architectures and objectives with adaptation.** This discrepancy motivates us to explore the practice of adaptation (i.e. extending the pretraining of a model with a different architecture/objective) as a way to efficiently obtain both a model suited to generative use cases and to mutitask finetuning
- **Finding 1.** Causal decoder-only models pretrained with a full language modeling objective achieve best zero-shot generalization when evaluated immediately after unsupervised pretraining , in line with current common practices for large language models.
- **Finding 2.** Encoder-decoder models trained with masked language modeling achieve the best zero-shot performance after multitask finetuning . More broadly, approaches that perform well in the single-task finetuning setting perform well on multitask finetuning.
- **Finding 3.** Decoder-only models can be efficiently adapted from one architecture/objective prior to the other. Specifically, to obtain both a generative and a multitask model with the smallest total compute budget possible, we recommend starting with a causal decoder-only model, pretraining it with a full language modeling objective, and then using non-causal masked language modeling adaptation before taking it through multitask finetuning .
---
### Secondary Contribution
 - [Model-link](https://github.com/bigscience-workshop/architecture-objective.)
---
### Limitations/Future Work
---
### Notes (Try to use backlinks)
- Recently, Sanh et al. [2021] proposed a multitask finetuned encoder-decoder LLM that outperforms decoder-only models on zero-shot generalization, despite being an order of magnitude smaller
- It has repeatedly been shown that an MLM objective produces a better pretrained model for subsequent supervised finetuning in transfer learning settings [Devlin et al., 2018, Lample and Conneau, 2019, Voita et al., 2019, Raffel et al., 2020].
- In a causal decoder, each token attends to the previous tokens only. In both non-causal decoder and encoder-decoder, attention is allowed to be bidirectional on any conditioning information. For the encoder-decoder, that conditioning is fed into the encoder part of the model
- we propose to study the opposite adaptation: starting from a causal decoder pretrained with FLM, we cast the model into a non-causal decoder (again by switching the attention mask) and we extend pretraining with MLM. We call this approach non-causal MLM adaptation (NC-A) ; to our knowledge, this is an entirely novel practice.
- On both our evaluation benchmarks, the causal decoder architecture systematically outperforms the other architectures when using language modeling pretraining alone. The non-causal decoder remains within a percent of the causal decoder performance, but the encoder-decoder performance lags far behind
- Our experimental study has led us to conclude the optimal architecture and objective choice for zero-shot performance depends on whether or not the model will ultimately undergo multitask finetuning: while a decoder-only model trained with full language modeling achieves the best zeroshot performance after unsupervised pretraining only, an encoder-decoder with masked language modeling is best once multitask finetuning is applied
- ![[2022_WhatArchitecture_ZeroShot_process.png]]
---
