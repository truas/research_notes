### Constrained Abstractive Summarization: Preserving Factual Consistency with Constrained Generation
---
- [Zotero Select Link](zotero://select/groups/2480461/items/ZBR8LMGR)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/ZBR8LMGR)
- Authors: [[Yuning Mao]] [[Jiawei Han]] 
- Topics: [[nlp_lm]] [[nlp_text_summarization]] [[nlp_constrain]] [[nlp_transformers]]
- Venue: #arXiv 
- Year: #2021
---
### Major Contributions
- “In this paper, we propose Constrained Abstractive Summarization (CAS), a more general setup where a set of tokens are used as constraints and required to be present in the summary. We show that CAS improves lexical overlap and factual consistency of abstractive summarization simultaneously.” (Mao et al., 2021, p. 1)
	- “ (1)automatic summarization without human involvement, where we extract keyphrases from the source document and use them as constraints; 
	- (2) humanguided interactive summarization, where human feedback in the form of manual constraints are used to guide CAS towards human preferences” (Mao et al., 2021, p. 2)
- They keep a list of constrains (extracted keywords) and make sure the generation use/correct them before EOS. If not the sequence is not finished.
---
### Secondary Contribution
---
### Limitations/Future Work
---
### Notes (Try to use backlinks)
- “one can conduct CAS on (almost) any fine-tuned models without (often expensive) re-training.” (Mao et al., 2021, p. 2)
- “BERTSum under CAS achieves better performance than more expensive methods such as BART (Lewis et al., 2019) and PEGASUS (Zhang et al., 2020a) by simply using one manual constraint during inference,” (Mao et al., 2021, p. 2)
- Constrains:
	-  “First, one can create the constraints automatically without human involvement, where the keyphrases in the source document are natural choices for constraints to preserve factual consistency (Sec. 2.2.1). 
	-  Second, for interactive summarization, when an automatic summary contains factual errors or lacks certain information, a human editor can manually add the corrected or missing facts as constraints during post-editing” (Mao et al., 2021, p. 2)
	-  “At a high level, DBA divides the beam during beam search to store hypotheses satisfying different numbers of constraints and adds unmet constraints at each decoding step. DBA ensures the presence of constraints by allowing the EOS token only when all the constraints are met. We choose DBA due to its faster speed than other counterparts (Hokamp and Liu, 2017)” (Mao et al., 2021, p. 3)
		-  “DBA completely functions during inference and can be easily incorporated into different models for the evaluation under CAS, which is preferable over methods that modify the training process” (Mao et al., 2021, p. 3)
	-  “by using only one phrase as guidance during inference without additional training (Phrase-4), CAS improves BERTSum up to 13.8 in ROUGE-2, outperforming state-of-the-art method” (Mao et al., 2021, p. 4)
---
