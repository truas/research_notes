### Do Language Models Plagiarize?
---
- [Zotero Select Link](zotero://select/groups/2480461/items/7EXFZPRI)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/7EXFZPRI)
- Authors: [[Jooyoung Lee]] [[Dongwon Lee]] 
- Topics: [[nlp_ppd]] [[nlp_lm]] [[nlp_transformers]]
- Venue: #arXiv
- Year: #year
---
### Major Contributions
- we investigate whether they not only memorize but also plagiarize training samples when generating artificial texts. Our findings support that they, especially GPT-2, reuse particular pieces of texts from the training corpus with or without obfuscation
	- 1) language models with more capacity plagiarize more;
	- 2) fine-tuned language models demonstrate differing patterns of plagiarism based on characteristics of auxiliary data; 
	- 3) sampling from truncated language modeling distributions tends to heighten the degree of plagiarism as opposed to temperature sampling,
	- 4) plagiarism in language models can have serious privacy consequences.
- To what extent do language models directly and indirectly exploit phrases or sentences in training samples?
	- (RQ1) Do pre-trained language models plagiarize? and 
	- (RQ2) Do finetuned language models plagiarize?.
---
### Secondary Contribution
- Attributes that mpact plagiarism: 
	- 1) Model size: Amongst four GPT-2 family, larger models (GPT-2 large and xl) plagiarize more from a training set than smaller models; 
	- 2) Fine-tuning Data: There is a positive correlation between document similarity levels between pre-training and fine-tuning sets and plagiarism; 
	- 3) Decoding methods and values of their parameters: Plagiarism cases differ depending on decoding approaches and parameter values.

- We apply a notion of plagiarism to an NLG task from both pre-trained and fine-tuned LMs.
- We develop an automatic plagiarism detection pipeline, which leverages the state-of-the-art BERT-based classifier and Named Entity Recognition (NER)
- We empirically highlight that risks related to memorization are underestimated. A Language model does more than copy and paste training samples; it can further rephrase sentences
---
### Limitations/Future Work
- As part of future work, we will quantitatively compare topical variations of these datasets and validate our assumption
- our findings are based on one particular language model, GPT-2, and thus may not generalize to other models such as GPT-3 and T5
	- Future work can revisit the proposed research questions on more diverse neural language models.
- our plagiarism type detection pipeline employs additional strict restrictions, especially on paraphrase detection, to minimize false positives
- 
---
### Notes (Try to use backlinks)
- A distinction between machine-authored and human-written content has even become quite challenging (Clark et al., 2021; Uchendu et al., 2020).
- through membership inference attacks, Carlini et al. (2021) could extract 32 memorized examples with individuals’ contact information out of 604 GPT-2 generated samples. The authors have also confirmed that models’ copying behaviors are prone to get worse as both the size of LMs and their training data increase
- recent studies (Lee et al., 2021; Kandpal et al., 2022) have shown that training data of language models tend to contain a large number of near-duplicates, and overlapping phrases included in near-duplicates significantly account for memorized text sequences.
- [Link GPT Output-dataset](https://github.com/openai/ gpt-2-output-dataset)
- Larger LMs plagiarize more. Consistent with (Carlini et al., 2021) and (Carlini et al., 2022), we find that larger models (large and xl) generally generate plagiarized sequences more frequently than smaller ones.
- Fine-tuning with an auxiliary dataset has varying impacts on plagiarism of LMs based on its characteristics. Our findings highlight that fine-tuning a model with an auxiliary data can mitigate memorization from the pre-training dataset. 
- Decoding methods and parameters affect plagiarism. Varying effects of decoding methods and their parameters on text quality and diversity have been extensively studied (DeLucia et al., 2020; Dou et al., 2021; Basu et al., 2020), but not from the plagiarism perspective.
	- top-p sampling is reported to be the most effective decoding method in various generation settings (Ippolito et al., 2019a; Zhang et al., 2020).
- Plagiarism can pose privacy harms. Our findings add value to ongoing discussions around privacy breaches resulting from the memorization of deep neural language models.
---
