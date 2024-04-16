### Unifying Language Model Paradigms
---
- [Zotero Select Link](zotero://select/groups/2480461/items/KY4WZED5)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/KY4WZED5)
- Authors: [[Yi Tay]] [[(optional) relevant author]] [[Donald Metzler]] 
- Topics: [[nlp_lm]]
- Venue: #arXiv 
- Year: #2022
---
### Major Contributions
- This paper presents a unified framework for pre-training models that are universally effective across datasets and setups.
	- We then propose Mixture-of-Denoisers (MoD), a pre-training objective that combines diverse pre-training paradigms together
	- [Their T5X model](https: //github.com/google-research/google-research/tree/master/ul2.)
	- [UL2](https://github.com/google-research/google-research/tree/master/ul2)
---
### Secondary Contribution
- X-Denoising is Complementarily Effective but Does Not Suffice as a Standalone
- Small Amounts of S-Denoisers is Preferred
- 
---
### Limitations/Future Work
- the switching denoising approaches is not clear. How do they actualyl switch during training and inference? the latter seems to be set via a parameter, but no the former.
	- R:Apparently all tasks as used in pre-training with a label and then associated during fine tuning/testing
- Results on GENIE for the 20B model is not better than humans even though they claim it is. See Table 8.
- A slight disclaimer is that we finetuned and trained this model on TPUv4 chips on our internal systems. Even so, finetuning would also sometimes result in nans which may require some care and manual tuning to get resolved. Therefore, if checkpoints were to be ported to another system, we could not guarantee that these checkpoints would work as well - "slight" 
---
### Notes (Try to use backlinks)
- why should the choice of the pre-trained LM depend on the downstream task? and how can we pre-train models that work universally well across many tasks?
- the newly proposed **Mixture-of-Denoisers (MoD),** a pre-training objective that enables strong performance across tasks. MoD is a mixture of several well-established denoising objectives along with new ones (X-denoising, S-denoising, R-denoising); x-> extreme language modeling; s->sequential/pre-fix language modeling; r->regular denoising, short spans and low corruption.
	- We opt to select models that predict the next target token instead of those that do so in-place (e.g., predict the current masked token in BERT) because the next-target formulation is more general and can subsume more tasks instead of using a special “CLS” tokens and task-specific projection heads.
	- **R-Denoiser -** The regular denoising is the standard span corruption introduced in Raffel et al. (2019) that uses a range of 2 to 5 tokens as the span length, which masks about 15% of input tokens
	- **S-Denoiser** - A specific case of denoising where we observe a strict sequential order when framing the inputs-to-targets task, i.e., prefix language modeling. To do so, we simply partition the input sequence into two sub-sequences of tokens as context and target such that the targets do not rely on future information (similar to casual LM)
	- **X-Denoiser** - An extreme version of denoising where the model must recover a large part of the input, given a small to moderate part of it. This simulates a situation where a model needs to generate long target from a memory with relatively limited information. To do so, we opt to include examples with aggressive denoising where approximately 50% of the input sequence is masked.
- UL2 outperforms GPT-3 175B on zero shot SuperGLUE.
- On one-shot summarization, UL2 triples the performance of an LM adapted T5 XXL model and is competitive with (or outperforms) PaLM and LaMDA at the same compute cost.
- UL2 outperforms by T5 +43.4% and +76.2% when compared to the GPTlike CLM decoder model. This is the highest relative (overall) gain compared to all other alternatives. We also note that on all individual tasks, UL2 outperforms T5 on all 9 out of 9 considered tasks. Hence, UL2 is a universally better option compared to the span corruption T5 mode
- ![[2022_UnifyingLM_UL2_Arch.png]]
- ![[2022_UnifyingLM_UL2_denoising.png]]
---
